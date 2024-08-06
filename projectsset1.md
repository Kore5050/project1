# project related to Dom

## project link
[click here]()

## project 1

```javascript
console.log("laxmikant");

const buttons=document.querySelectorAll(".button");
const body=document.querySelector("body"); 
buttons.forEach(function(button){
    console.log(button)
    button.addEventListener('click',function(e){
        console.log(e)
        console.log(e.target)
        if(e.target.id==="orange"){
            body.style.backgroundColor=e.target.id; 
        }
        if(e.target.id==='white') {
            body.style.backgroundColor=e.target.id; 
            
        }
        if(e.target.id==='green'){
            body.style.backgroundColor=e.target.id; 
       }
       if(e.target.id==='yellow'){
        body.style.backgroundColor=e.target.id; 
       }
       if(e.target.id==='red'){
        body.style.backgroundColor=e.target.id; 
       }

    })
})

## project 2

const form=document.querySelector('form');
form.addEventListener('submit',function(e){
    e.preventDefault();
    const height=(document.querySelector('#height').value)
    const weight=(document.querySelector('#weight').value)
    const results=document.querySelector('#results')

    if(height===''|| height<0 || isNaN(height)){
        results.innerHTML=`please give a valid height ${height}`

    }
    if(weight===''|| weight<0 || isNaN(weight)){
        results.innerHTML=`please give a valid weight ${weight}`
    }
    else{
        const bmi=(weight / ((height*height)/10000)).toFixed(2);
        // show the result
        results.innerHTML= `<span>${bmi}</span>`
    }

});
```