# Practice Manipulating the DOM
// 1: Set the text of the <h1> element
const h1 = document.querySelector('h1');
h1.textContent = 'BABA';

// 2: Set the color of the <h1> to a different color
h1.style.color = 'pink';

// 3: Set the content of the '.desc' paragraph
// The content should include at least one HTML tag
let contentDesc = document.querySelector('.desc');
contentDesc.innerHTML = '<h3>bobo</h3>';

// 4: Set the class of the <ul> to 'list'
const ul = document.querySelector('ul');
ul.className = 'list';

// 5: Create a new list item and add it to the <ul>
const newList = document.createElement('li');

//const input = document.createElement('input');
//newList.textContent = ' new';
//newList.prepend(input);

newList.innerHTML = "<input> New";
ul.appendChild(newList);

// 6: Change all <input> elements from text fields to checkboxes

const checkBox = document.querySelectorAll('input');
for (let i = 0; i<checkBox.length; i++){
  checkBox[i].type = 'checkbox';
};

// 7: Create a <button> element, and set its text to 'Delete'
// Add the <button> inside the '.extra' <div>
const extra = document.querySelector('.extra');

const btn = document.createElement('BUTTON');
btn.textContent = 'Delete';
extra.appendChild(btn);

console.log('btn');

// 8: Remove the '.extra' <div> element from the DOM when a user clicks the 'Delete' button
btn.addEventListener('click', () =>{
                     const p = extra.querySelector('p');
                     extra.remove();
                     });
