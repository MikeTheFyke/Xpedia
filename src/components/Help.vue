<template>
    <div>
        <div id="Help-Container" v-on:click="expand" @mouseover="buttonPopUp" @mouseleave="buttonUnPop">
            <div id="Help-Image"></div>
            <h1 id="Help-Text">Help</h1>
        </div>
        <div id="Help-Window">
            <div id="Help-Conversation-Container">
                <h1 id="Help-Conversation-Text"></h1>
                <ul id="My-Conversation">
                </ul>
            </div>
            <div id="Help-Header">
                <h1 id="Help-Header-Heading">How can we help?</h1>
                <div id="Help-Close" v-on:click="expand">X</div>
            </div>
            <div id="Message-Input">
                <input id="Text-Input" type="text" placeholder="Please enter your message" @keyup.enter="messageAdd">
                <input id="Submit-Input" type="submit" value=">" v-on:click="messageAdd">
            </div>
        </div>
    </div>
</template>

<script>
import TweenMax  from 'gsap';

export default {
    name: 'Help',
    data(){
        return{
            clicked: false,
            date: new Date(),
            message: "",
            newMessage: "",
        }
    },
        mounted: function(){
        TweenMax.to("#Help-Window", 0, {opacity:0, zIndex: -1});
        document.getElementById('Help-Conversation-Text').innerText = this.date.toDateString();
    },
    methods:{
        expand(){
                if (this.clicked === false){
                    document.getElementById('Text-Input').focus()
                    TweenMax.to("#Help-Window", 0.25, { opacity:1, zIndex: 5 })
                    TweenMax.to("#Help-Container", 0.25, { y: "10vh", opacity: 0})
                    this.clicked = true
                } else {
                    document.getElementById('Text-Input').blur()
                    TweenMax.to("#Help-Window", 0.25, { opacity:0, zIndex: -1 })
                    TweenMax.to("#Help-Container", 0.25, { y: 0, opacity: 1})
                    this.clicked = false
                }
        },
        buttonPopUp(){
            TweenMax.to("#Help-Container", 0.25, { scale:1.5 })
        },
        buttonUnPop(){
            TweenMax.to("#Help-Container", 0.25, { scale:1 })
        },
        messageAdd(){
            this.date = new Date();
            this.message = document.getElementById("Text-Input").value;
            console.log(this.message)
            this.newMessage = this.date.toLocaleTimeString() + " - " + this.message;
            console.log(this.newMessage)

            var node = document.createElement("LI");
            var NewMessage = document.createTextNode(this.newMessage)
            node.appendChild(NewMessage)
            document.getElementById("My-Conversation").appendChild(node)
            document.getElementById("Text-Input").value = ""
            
        },
    }    
}
</script>

<style scoped>

#Help-Container{
    position: fixed;
    bottom: 30px;
    right: 30px;
    width: 100px;
    height: 40px;
    border-radius: 20px;
    background-color: white;
    box-shadow: 2px 6px 10px 0px #dfe3e6;
    display: flex;
    justify-content: space-around;
    cursor: pointer;
}

#Help-Image{
    height: 20px;
    width: 20px;
    border-radius: 5px;
    background-color: teal;
    margin: 10px 0px 0px 5px;
}

#Help-Text{
    color: teal;
    font-family: "Montserrat";
    font-size: 16px;
    margin-right: 5px;
}

#Help-Window{
    position: fixed;
    bottom: 60px;
    right: 30px;
    width: 400px;
    height: 600px;
    border-radius: 15px;
    background-color: white;
    box-shadow: 2px 6px 10px 0px #dfe3e6;
    overflow: hidden;
}

#Help-Header{
    position: absolute;
    top: 0px;
    width: 100%;
    height: 50px;
    background-color: #e3c624;
    text-align: center;
}

#Help-Header-Heading{
    color: black;
    font-family: "Montserrat";
    font-size: 16px;
}

#Help-Close{
    position: inherit;
    top: 10px;
    right: 15px;
    height: 20px;
    width: 20px;
    color: black;
    font-family: "Montserrat";
    font-size: 18px;
    cursor: pointer;
}

#Message-Input{
    position: absolute;
    bottom: 0px;
    width: 100%;
    height: 50px;
}

#Text-Input{
 width: 80%;
 height: 20px;
 outline: none;
 margin-left: 2%;
 border-radius: 5px;
 border-color: #dfe3e6;
 border-style: solid;
}

#Text-Input::placeholder{
    color: #dfe3e6;
}

#Submit-Input{
    width: 15%;
    color: teal;
    font-family: "Montserrat";
    font-size: 20px;
    background-color: transparent;
    border-style: none;
    outline: none;
    cursor: pointer;
}

#Help-Conversation-Container{
    position: absolute;
    top: 50px;
    width: 100%;
    color: #b3b1ab;
    font-family: "Montserrat";
    font-size: 10px;
}

#Help-Conversation-Text{
    color: teal;
    font-family: "Montserrat";
    font-size: 14px;
    width: 90%;
    margin: 0 35% 0 35%;
}

#My-Conversation{
    color: black;
    font-family: "Montserrat";
    font-size: 10px;
    list-style-type: none;
    margin: 10px 10px 10px 10px;
    padding: 0;
}

</style>