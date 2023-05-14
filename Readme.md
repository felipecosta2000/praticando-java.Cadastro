## JSE --> java local 
##control --> pacote de Controle (logica)
## entity --> pacote de Classes de Banco de Dados
## view --> entrada e saÃ-da (WEB)
## persistence --> banco de dados
## io --> gravacao txt, xml, json 
===========
Classe Cliente
package entity; //pacote
public class Cliente { //classe
//int , long, float, double (tipos primitivos) 
//Integer, Long, Float, Double (Wrappers) 
private Long id; //atributo
private String nome;

private String email;
private String sexo;
//saÃ-da
public Long getId() {
return id;
}
//entrada
public Cliente setId(Long id) {
this.id = id;
return this;
}
//saÃ-da do Nome
public String getNome() {
return nome;
}
//entrada do nome
//Pattern Builder // cascate ...
public Cliente setNome(String nome) {
this.nome = nome;
return this;
}
public String getEmail() {
return email;
}
 //void (acao) nao tem o retorno
public void setEmail(String email) {
//if (this.email.equals("profedsobelem@gmail.com")) 
// return; //se o email tal fim
this.email = email;
}
public String getSexo() {
return sexo;
}
public Cliente setSexo(String sexo) {
this.sexo = sexo;
return this;
}
//alt + s generated getter and setter
//main + ctrl + espaco e enter
public static void main(String[] args) {
//testar (executar)

//Classe objeto = espaÃ§o de Mem executando o 
construtor..
Cliente c= new Cliente();
//Classe objeto (espaÃ§o de Mem) Programa que
inicializa (Construtor)
//ctrl + shift + s (salvar)
 //
 //encapsulou
 c.setNome("jose").
 setId(10L).
 setSexo("m").
 setEmail("jose@gmail.com");
 //syso (atalho da impressao)
 //sysout
 System.out.println(c.getNome() + ", "+ c.getSexo());
 // + concatenar (ao Lado) 
 // + conversao em String
 //ctrl + f11
}
return "Cliente [id=" + id + ", nome=" + nome + ", email=" 
+ email + ", sexo=" + sexo + ", op=" + op + "]";
=========================
package entity; //pacote
public class Cliente { // classe
// int , long, float, double (tipos primitivos)
private Long id;
private String nome;
private String email;
private String sexo;
private String op;
// cosntrutor cheio (encapsula tudo de uma vez)
// Opcao de Escolha
// opcao de Sobrecarga de Construtores ...
public Long getId() {
return id;
}
// escolha = sobrecarga
public Cliente(Long id, String nome, String email, String 
sexo) {
this.id = id;
this.nome = nome;
this.email = email;
this.sexo = sexo;
}
public String toString(){
if (this.op.equals("txt")) {
return this.id + "," + this.nome +"," + 
 this.email + ","+ this.sexo;
}else if (this.op.equals("json")) {
return "{\"id\":" + this.id + 
",\"nome\":" + this.nome + "}";
}else {
//retorna o padrÃ£o dele
 return "Cliente [id=" + id + ", nome=" + nome +
 ", email=" + email + ", sexo=" + sexo + "]";
}
}
public Cliente() {
}
public Cliente setId(Long id) {
this.id = id;
return this;
}
public String getNome() {
return nome;
}
public Cliente setNome(String nome) {
this.nome = nome;
return this;
}
public String getEmail() {
return email;
}
// void (acao) nao tem o retorno
public void setEmail(String email) {
// if (this.email.equals("profedsobelem@gmail.com"))
// return; //se o email tal fim
this.email = email;
}
public String getSexo() {
return sexo;
}
public Cliente setSexo(String sexo) {
this.sexo = sexo;
return this;
}
// alt + s generated getter and setter
// main + ctrl + espaco e enter
public String getOp() {
return op;
}
public void setOp(String op) {
this.op = op;
}
public static void main(String[] args) {
// testar (executar)
// Classe objeto = espaÃ§o de Mem executando o 
construtor..
// Cliente c= new Cliente();
// Classe objeto (espaÃ§o de Mem) Programa que
inicializa (Construtor)
// ctrl + shift + s (salvar)
//
// encapsulou
// c.setNome("jose").
// setId(10L).
// setSexo("m").
// setEmail("jose@gmail.com");
// syso (atalho da impressao)
// sysout
// System.out.println(c.getNome() + ", "+ 
c.getSexo());
// + concatenar (ao Lado)
// + conversao em String
// ctrl + f11
// ctrl + shift + c
 //Encapsulamento dos dados set e get e o Construtor ...
Cliente c = new Cliente(10L, "veloz", 
 "veloz@gmail.com", "m");
System.out.println(c.getNome() + ", "
 + c.getEmail() + ", " + c.getSexo() +
 ", " + c.getId());
}
}
