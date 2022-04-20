# Javascript_ES6
learb more of javascript es6

# Varables
var 
let 
const

global varables
are on top of a scope, outside the functions.

# Void, null, empty, undefine
    -- null -> indicate that the is no value

# Truthiness 

Implicit
    if(true)
    {

    }
    if(1)
    {

    }
    if('true')
    {

    }
    if('false')
    {

    }

Explicit

    if(Boolean('false'))
    {

    }

# Ternary operator

let someVar

someVar = (true) ? true : true

What is above is the same with below

if(true) {
    someVar = true
}else {
    someVar = false
}

# Modulus operator

# Nullish coalescing operator
|| or

var pick_a_number

pick_a_number = pick_a_number || Math.floor(Math.random()* arrar)

# try ,catch , finally
# Transpiling
# Spread syntax
Let say you want to work with two object sonrt it by name

let dogs = [
        {
            name: 'pugsley', scr:'img/pugsley.png'},
            name: 'Mojo' src: 'ima=g/mojo.png'}
        }
    ];

let cats = [
    {
        name: 'Sniggles', scr:'img/Sniggles.png'},
        name: 'Roo' src: 'img=g/roo.png'}
    }
];

let domEl = document.querySelector('#doglist);

let inventory = [...dogs, ...cats]
    .sort((a, b) => a.name.toLowerCase() <
    b.name.toLowerCase() ? -1 : 1);

for (let pet of inventory) {
    let image = document.createElement('img);
    image.src = pet.src;
    image.alt = pet.name;
    domEl.appendChild(image);
}

# Promises

const myPromise = new Promise(
    function (resolve, reject) {
        if(true === true)
        {
          resolve('True Message')  
        }else{
            reject('false Message')
        }
    })

myPromise
.then(function (message) {
    console.log(message)
})
.catch(function (message) {
    console.log(message)
})
.finnally(function (message) {
        console.log(message)
})

const exercise = ['a','b','c','d','e','d','e'];
const trainBtn = document.querySelector('#train');
const pic = document.querySelector('#pic')

trainBtn.addEventListener('click', () => {
    const whichOne = 
    Math.floor(Math.random() * exercise.length)
    pic.src = './img/${exercise{whichOne}}.svg'
    trainBtn.value = exercise[whichOne]
    trainBtn.disabled = true
    new Promise((resolve) => setTimeout(resolve, 5000))
    .then(() => {
        pic.src = ''
        trainBtn.value = 'next'
        trainBtn.disabled = false
    })
});

# Async/await

const MyPromise = new Promise((resolve) =>
setTimeout(() => {
    resolve('Success');
}, 2000);
});

async function myAsync() {
    console.log('Before Promise');
    const result = await myPromise;
    console.log(result);
    console.log('After Promise')
}

console.log('Before myAsync');
myAsync();
console.log('After myAsync');

const exercise = ['a','b','c','d','e','d','e'];
const trainBtn = document.querySelector('#train');
const pic = document.querySelector('#pic')

trainBtn.addEventListener('click', async() => {
    const myPause = new Promise((resolve) => 
    setTimeout(resolve, 5000))

    const whichOne = Math.floor(Math.random() * exercise.length)

    pic.src = './img/${exercise{whichOne}}.svg'
    trainBtn.value = exercise[whichOne]
    trainBtn.disabled = true

    await myPause

        pic.src = ''
        trainBtn.value = 'next'
        trainBtn.disabled = false
    
});