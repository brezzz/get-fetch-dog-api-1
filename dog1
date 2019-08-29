'use strict';

function getDogImage() {
const amountEntry = $('.breed-type-entry').val(); 
console.log('Line 5 in index.js - amountEntry is: ' + amountEntry );
    if (amountEntry < 1) {
fetch(`https://dog.ceo/api/breeds/image/random/3`)
          .then(response => response.json())
          .then(responseJson => 
            displayResults(responseJson))
              .catch(error => alert('Something went wrong. Try again later.'))
      console.log('The amount entered is less than 1')

        } else if (amountEntry >= 1 && amountEntry < 51) {


    
          fetch(`https://dog.ceo/api/breeds/image/random/${amountEntry}`)
          .then(response => response.json())
          .then(responseJson => 
            displayResults(responseJson))
              .catch(error => alert('Something went wrong. Try again later.'))
              }
           else {

console.log('N/A, Unhappy Case ');
alert('Unhappy Case: Please chose a number less than 51 and try again.');
           }   
              ;
}
function displayResults(responseJson) {
  console.log(responseJson.message);
  //replace the existing image with the new one
jQuery.each( responseJson.message, function( i, val ) {
  $('.results-img').html(
    `<img src="${val}" class="results-img">`+ '' )
});


  //display the results section
  $('.results').removeClass('hidden');
}



function watchForm() {
  $('form').submit(event => {
    event.preventDefault();
    getDogImage();
  });
}

$(function() {
  console.log('App loaded! Waiting for submit!');
  watchForm();
});
