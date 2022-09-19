# Caesars_Cipher
Javascript
  
const alphabet = [  
&ensp;  "A",  
&ensp;  "B",  
&ensp;  "C",  
&ensp;  "D",  
&ensp;  "E",  
&ensp;  "F",  
&ensp;  "G",  
&ensp;  "H",  
&ensp;  "I",  
&ensp;  "J",  
&ensp;  "K",  
&ensp;  "L",  
&ensp;  "M",  
&ensp;  "N",  
&ensp;  "O",  
&ensp;  "P",  
&ensp;  "Q",  
&ensp;  "R",  
&ensp;  "S",  
&ensp;  "T",  
&ensp;  "U",  
&ensp;  "V",  
&ensp;  "W",  
&ensp;  "X",  
&ensp;  "Y",  
&ensp;  "Z"  
];  
  
function rot13(str) { //SERR PBQR PNZC  
&ensp; //create accumulator  
&ensp; let accumulator = "";  
  
&ensp;  //loop through the string  
&ensp;  for (let i = 0; i < str.length; i++) {  
&emsp;    const char = str[i];  
&emsp;    const isALetter = alphabet.includes(char);  
      
&emsp;    //if character is not a letter, add to the accumulator  
&emsp;    if (isALetter === false){  
&emsp;      accumulator += char;  
&ensp;    } else{  
&emsp;     //else, rotate + or - 13, add to accumulator  
&emsp;      const charIndex = alphabet.findIndex((c) => c === char);  
&emsp;  
&emsp;      accumulator += alphabet [charIndex + 13] ||  
&emsp;          alphabet [charIndex - 13];  
&ensp;    }  
&ensp;      
&ensp;  }  
  
&ensp;  return accumulator;  
  
}  

rot13("SERR PBQR PNZC");  
