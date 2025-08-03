# Project Related to DOM

## Project Link 
[click here]()

# Solution Code

## Project 3

``` 
Java Script 

const clock = document.querySelector('.clock')
console.log(clock)

 // It is use to print local time

// setInterval() // It say's give me a method , And also tell me 
// the interval ,that after how many time you want too countinously run ,  
// until the program is running. 

// Imporatant syntax for set interval 
//1000 - 1 second
// setInterval(function(){},1000)

let h = document.querySelector('#hours')
let m = document.querySelector('#minutes')
let s = document.querySelector('#seconds')
let period = document.querySelector('#period')
setInterval(function(){
  let date = new Date()
  // Convert to 12-hour format
                let hours = date.getHours()
                let hours12 = hours % 12;
                hours12 = hours12 === 0 ? 12 : hours12; 

// f you want the output to always show two digits (like "03" instead of "3"),
let formattedHours = String(hours12).padStart(2, '0'); 
let min = date.getMinutes();
let formattedMinutes = String(min).padStart(2, '0');
let sec = date.getSeconds();
let formattedSeconds = String(sec).padStart(2, '0');
      

    h.innerHTML = formattedHours
    m.innerHTML = formattedMinutes
    s.innerHTML = formattedSeconds
// let hours1 = hours % 12 || 12; // Converts 0 to 12
let per = hours >= 12 ? "PM" : "AM";
period.innerHTML =  per
},1000)


```
