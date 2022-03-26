aluno.java
public class Aluno {
    private String nome;
    private int ra;
    private char sexo;
    private String rg;
    private String cpf;
    private Data dataNascimento;

    public Aluno(String nome, int ra, char sexo, String rg, String cpf, Data dataNascimento) {
        this.nome = nome;
        this.ra = ra;
        this.sexo = sexo;
        this.rg = rg;
        this.cpf = cpf;
        this.dataNascimento = dataNascimento;
    }

    public Data getDataNascimento() {
        return dataNascimento;
    }   
    public String getNome() {
        return nome;
    }

    public int getRa() {
        return ra;
    }

    public char getSexo() {
        return sexo;
    }

    public String getRg() {
        return rg;
    }

    public String getCpf() {
        return cpf;
    }

    public void setNome(String nome) {
        this.nome = nome;
    }

    public void setRa(int ra) {
        this.ra = ra;
    }

    public void setSexo(char sexo) {
        this.sexo = sexo;
    }

    public void setRg(String rg) {
        this.rg = rg;
    }

    public void setCpf(String cpf) {
        this.cpf = cpf;
    }
    public void imprimir(){
        System.out.println(ra);
        System.out.println(nome);
        System.out.println(sexo);
        System.out.println(rg);
        System.out.println(cpf);
        System.out.println(dataNascimento.formatarData());
    }
    
}

data.java
public class Data {
    private int dia;
    private int mes;
    private int ano;

    public Data(int data, int mes, int ano) {
        this.dia = data;
        this.mes = mes;
        this.ano = ano;
    }

    public int getDia() {
        return dia;
    }

    public int getMes() {
        return mes;
    }

    public int getAno() {
        return ano;
    }

    public void setDia(int dia) {
        this.dia = dia;
    }

    public void setMes(int mes) {
        this.mes = mes;
    }

    public void setAno(int ano) {
        this.ano = ano;
    }
    public String formatarData() {
    return dia + "/"+ mes + "/" + ano; 
    }
}

teste.java
public class Teste {

    /**
     * @param args the command line arguments
     */
    public static void main(String[] args) {
        Data data = new Data(10,10,1990);
        Aluno cli = new Aluno("Dionisio", 2543823, 'M', "573666212312", "470321141122",data );
        cli.imprimir();

    }

}
