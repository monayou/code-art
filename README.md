var imgBurger;
var imgMouth;
var imgEyes;
var imgKitchen;
var arr = [];


function preload() {
    imgBurger = loadImage("Burger.png");
    imgMouth = loadImage("mouth.png");
    imgEyes = loadImage("Eyes.png");
    imgKitchen = loadImage("Kitchen.png");

}

function setup() {
    createCanvas(1600, 900);
}

function draw() {
    image(imgKitchen, 0, 0);
    image(imgEyes, 400, 100);
    image(imgMouth, 500, 500);
    textSize(70);
    text("Feed me", 570, 430, 500, 500);
    for (i = 0; i < arr.length; i+=2) {
        image(imgBurger, arr[i], arr[i+1]);
    } 
    image(imgBurger, mouseX, mouseY);
}

function mouseClicked() {
    arr.push(mouseX, mouseY);
}
