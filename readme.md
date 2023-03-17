# style.css
* {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
}
body {
    background: #55a0dd;
    height: 100vh;
    width: 100%;
    display: flex;
    justify-content: center;
    align-items: center;
}
section {
    height: 500px;
    width: 600px;
}
.col {
    background-color: #fff;
    width: 100%;
    border-radius: 4px;
    padding: 5px;
    box-shadow: #00000059 0px 5px 15px;
}
.box {
    display: inline-block;
    padding: 0 5px;
}
.first {
    border-right: 2px solid #40576d33;
}
input[type=number] {
    outline: none;
    border: none;
    width: 50px;
    color: #131c35;
    font-size: 24px;
    padding: 10px 0px;
    margin-left: 10px;
}
.second {
    border-right: 2px solid #40576d33;
}
button {
    border: none;
    color: #131c35;
    font-size: 20px;
    font-weight: 300;
    background-color: transparent;
    padding: 10px 16px;
    border-radius: 3px;
    cursor: pointer;
    user-select: none;
}
button:hover {
    background-color: #40576d1a;
}
button.active {
    background-color: #73b1e333;
    color: #5271ff;
}
.third {
    border-right: 2px solid #40576d33;
}
.third button:focus {
    background-color: #73b1e333;
    color: #5271ff;
}
input[type=color] {
    width: 35px;
    outline: none;
    border: none;
    background: none;
}
textarea {
    width: 100%;
    height: 400px;
    padding: 10px;
    border-radius: 3px;
    outline: none;
    border: none;
    resize: vertical;
}







# app.js
const textarea = document.getElementById("textarea1");
function f1(e) {
    let value = e.value;
    textarea.style.fontSize = value + "px";
}
function f2(e) {
    if (textarea.style.fontWeight == "bold") {
        textarea.style.fontWeight = "normal";
        e.classList.remove("active");
    }
    else {
        textarea.style.fontWeight = "bold";
        e.classList.add("active");
    }
}
function f3(e) {
    if (textarea.style.fontStyle == "italic") {
        textarea.style.fontStyle = "normal";
        e.classList.remove("active");
    }
    else {
        textarea.style.fontStyle = "italic";
        e.classList.add("active");
    }
}
function f4(e) {
    if (textarea.style.textDecoration == "underline") {
        textarea.style.textDecoration = "none";
        e.classList.remove("active");
    }
    else {
        textarea.style.textDecoration = "underline";
        e.classList.add("active");
    }
}
function f5(e) {
    textarea.style.textAlign = "left";
}
function f6(e) {
    textarea.style.textAlign = "center";
}
function f7(e) {
    textarea.style.textAlign = "right";
}
function f8(e) {
    if (textarea.style.textTransform == "uppercase") {
        textarea.style.textTransform = "none";
        e.classList.remove("active");
    }
    else {
        textarea.style.textTransform = "uppercase";
        e.classList.add("active");
    }
}
function f9() {
    textarea.style.fontWeight = "normal";
    textarea.style.textAlign = "left";
    textarea.style.fontStyle = "normal";
    textarea.style.textTransform = "capitalize";
    textarea.value = "";
}
function f10(e) {
    let value = e.value;
    textarea.style.color = value;
}
window.addEventListener('load', () => {
    textarea.value = "";
});
