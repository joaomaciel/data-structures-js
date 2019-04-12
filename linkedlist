function ListaEncadeada() {
  this.cabeca = null;
  this.pe = null;
}
 
function No(value, next, prev) {
  this.value = value;
  this.next = next;
  this.prev = prev;
}
 
ListaEncadeada.prototype.addToCabeca = function(value) {
  var newNode = new No(value, this.cabeca, null);
  if (this.cabeca) this.cabeca.prev = newNode;
  else this.pe = newNode;
  this.cabeca = newNode;
};
 
ListaEncadeada.prototype.addToPe = function(value) {
  var newNode = new No(value, null, this.pe);
  if (this.pe) this.pe.next = newNode;
  else this.cabeca = newNode;
  this.pe = newNode;
};
 
ListaEncadeada.prototype.removeCabeca = function() {
  if (!this.cabeca) return null;
  var val = this.cabeca.value;
  this.cabeca = this.cabeca.next;
  if (this.cabeca) this.cabeca.prev = null;
  else this.pe = null;
  return val;
};
 
ListaEncadeada.prototype.removePe = function() {
  if (!this.pe) return null;
  var val = this.pe.value;
  this.pe = this.pe.prev;
  if (this.pe) this.pe.next = null;
  else this.cabeca = null;
  return val;
};
 
ListaEncadeada.prototype.search = function(searchValue) {
  var currentNode = this.cabeca;
  while (currentNode) {
    if (currentNode.value === searchValue) return currentNode.value;
    currentNode = currentNode.next;
  } 
  return null;
};
 
ListaEncadeada.prototype.indexOf = function(value) {
  var indexes = [];
  var currentIndex = 0;
  var currentNode = this.cabeca;
  while(currentNode) {
    if (currentNode.value === value) indexes.push(currentIndex);
    currentNode = currentNode.next;
    currentIndex++;
  }
  return indexes;
};
 
 
var myLL = new ListaEncadeada();
 
myLL.addToCabeca(123);
myLL.addToCabeca(70);
myLL.addToCabeca('joao');
myLL.addToPe(19);
myLL.addToPe('joao2');
myLL.addToPe(20);
console.log(myLL);
