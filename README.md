### console.log("Hello, World");

### const nome = 'Karol';
### let email = 'tecnologia.karol@gmail.com';
### console.log(`Nome: ${nome}  Email: ${email}`);

### if((nome == "Karol")){
###     console.log('Nome correto');
### }

### function escreve(x){
###     console.log("Frase:" + x);
### }

### escreve(`Seja bem vinda, ${nome}`);
### escreve("Treinamento HTML5, CSS3 e JS")

### console.log(`número de elementos: ${db.length}`);

### const frutas = ['banana', ' abacate', 'melância', 'abacaxi'];

### console.log(frutas.length);

### ### criando um objeto literal
### ### Padrão parecido com JSON, de modo a não incluir ações
### const dados = {
###     nome: 'Karol',
###     idade: 25,
###     programadora: true,
###     acao: (x,y)=>{
###         console.log(`Executando uma ação ${x+y}`);
###     }
### };
### console.log(dados.acao(15,7));

### ### Objeto é um conjunto de atributos (propriedade ou valores) e métodos (ações ou frutas)

### HTML para colocar um novo step na ultima tarefa

            <form id="addNewStep">
                <label for="inputTxtNewStep" draggable="true">
                    <svg xmlns="http://www.w3.org/2000/svg" height="20" width="20"><path fill="#fff" d="M9.375 13.875H10.625V10.625H13.875V9.375H10.625V6.125H9.375V9.375H6.125V10.625H9.375ZM10 17.75Q8.375 17.75 6.969 17.146Q5.562 16.542 4.51 15.49Q3.458 14.438 2.854 13.031Q2.25 11.625 2.25 10Q2.25 8.375 2.854 6.969Q3.458 5.562 4.51 4.51Q5.562 3.458 6.969 2.854Q8.375 2.25 10 2.25Q11.625 2.25 13.031 2.854Q14.438 3.458 15.49 4.51Q16.542 5.562 17.146 6.969Q17.75 8.375 17.75 10Q17.75 11.625 17.146 13.031Q16.542 14.438 15.49 15.49Q14.438 16.542 13.031 17.146Q11.625 17.75 10 17.75ZM10 10Q10 10 10 10Q10 10 10 10Q10 10 10 10Q10 10 10 10Q10 10 10 10Q10 10 10 10Q10 10 10 10Q10 10 10 10ZM10 16.5Q12.688 16.5 14.594 14.604Q16.5 12.708 16.5 10Q16.5 7.312 14.604 5.406Q12.708 3.5 10 3.5Q7.312 3.5 5.406 5.396Q3.5 7.292 3.5 10Q3.5 12.688 5.396 14.594Q7.292 16.5 10 16.5Z"/></svg>
                    <input type="text" id="inputTxtNewStep" placeholder="Adicionar nova step" />
                </label>
            </form>

### Adicionar novo step na última tarefa 

### const newStep = document.querySelector('#inputTxtNewStep');
### const forms = document.querySelector('#addNewStep');
### forms.addEventListener("submit", (a) => {
###     a.preventDefault();
### });
### newStep.addEventListener("keyup", (a) => {
###     a.preventDefault();
###     a.stopPropagation();
###     if(a.key == "Enter"){
###         alert(newStep.value);
###         console.log(db[db.length-1].keys);
###         if(db[db.length-1].hasOwnProperty('steps') == false){
###             db[db.length-1]['steps'] = [];
###         }        
###         db[db.length-1].steps.push({step: newStep.value});
###         newStep.value = "";
###         console.log(db);
###         console.log(db[db.length - 1].steps);
###     }    
### });