### TypeScript commands
<dl>
  <dt>CMD to Compile TypeScript</dt>
  <dd>tsc fileName.ts -w</dd>
  <dt>Complia e adiciona o watch</dt>
  <dd>Cada vez que actualiza o ficheiro cria o respectivo JS <em>fileName.js</em>.</dd>
  <dt>Add your .js file to the HTML file with:</dt>
  <dd><script src="fileName.js"></script></dd>
</dl>

## TypeScript 

```ts
let mySum = function(num1: any, num2:any):number {
  if (tyopeof num1 == 'string') {
    num1 = parseInt(num1);
  }
  if (typeof num2 == 'string') {
    num2 = parseInt(num2);
  }
  return num1 + num2;
}

console.log(mySum('3',5));

function getName (firstName: string, lastName?: string): string {
  if(lastName == undefined) {
    return firstName;
  }
  return firstName + " " + lastName;
}

console.log(getName('John'));

function myVoid(): void {
  return;
}

## Interfaces

/* function showTodo( todo: {title:string, text: string}) {
  console.log(todo.title+": "+todo.text);
  
}
let myTodo = {title: 'Trash', text: 'Take out trash'}
showTodo(myTodo); */

interface Todo{
    title: string;
    text: string;
}

function showTodo ( todo: Todo) {
  console.log(todo.title+": "+todo.text);
}

let myTodo = {title: 'Trash', text: 'Take out trash'}
showTodo(myTodo);

## Classes
interface UserInferface {
    name:string;
    email:string;
    age: number;
    register();
    payInvoice();
}
class User implements UserInterface{
    name: string;
    email:string;
    age: number;
    
    constructor(name: string, email:string, age: number) {
        this.name = name;
        this.email = email;
        this.age = age;
        
        console.log("User Created: " + this.name);
    }
    register() {
      console.log( this.name+" is now registered");
    }
    
    payInvoice() {
      console.log(this.name+ " Paid invoice");
    }
}

let john = new User('John Doe', 'emailJoe@gmail.com', 22);
john.register();
console.log(john.age);

class Member extends User {
    id: number;
    
    constructor(id: number, name: string, email:string, age: number) {
        super(name, email, age);
        this.id = id;
    }
    
    payInvoice(){
        super.payInvoice();
    }
}

let mike: User = new Member(1, 'Mike Smith','mike@gmail.com',33);
mike.payInvoice();



```
