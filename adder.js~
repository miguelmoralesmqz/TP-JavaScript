//Function adder
function adder(l, r){
  return function(v){
    return l(v) + r(v);
  }
}
//function mult
function mult(v){
  return function(e){
    return v*e;
  }
}
console.log("adder(mult(2), mult(4))(2) Resultat: "+adder(mult(2), mult(4))(2));

//Implémenter "sub(x)(y)" tel que: (1pt)
function sub(v){
  return function(e){
    return v-e;
  }
}

console.log("sub(0)(0) Resultat: "+sub(0)(0)); // 0
console.log("sub(2)(1) Resultat: "+sub(2)(1)); // 1
console.log("sub(2)(2) Resultat: "+sub(2)(2)); // 0
console.log("sub(2)(4) Resultat: "+sub(2)(4)); // -2

//Transformer la fonction adder pour qu'elle accepte un nombre variable d'argument tel que: (3pt)

function adder_2(){ 
 var args = Array.prototype.slice.call(arguments); 
 var a = 0; 
 return function(v){ 
     args.forEach(function(e){a+=e(v);}); 
     return a; 
 };
}
console.log("adder_2()(0) Resultat: "+adder_2()(0)); // 0
console.log("adder_2()(1) Resultat: "+adder_2()(1)); // 0
console.log("adder_2(mult(2))(1) Resultat: "+adder_2(mult(2))(1)); // 2
console.log("adder_2(mult(2), mult(2))(1) Resultat: "+adder_2(mult(2), mult(2))(1)); // 4
console.log("adder_2(mult(2), mult(2), mult(2))(1) Resultat: "+adder_2(mult(2), mult(2), mult(2))(1)); // 5
console.log("adder_2(mult(2), sub(2), mult(2))(1) Resultat: "+adder_2(mult(2), sub(2), mult(2))(1)); // 6

/*Vous utiliserez:
var args = Array.prototype.slice.call(arguments);
[1,2,3].forEach(function(val){console.log(val);});
*/


