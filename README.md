# codigos-
laluno= [] 
lemail= [] 
lcurso= [] 
todos = [laluno,lcurso,lemail] 
 
def menu (): 
    print ("Menu\n [1]Cadastrar novo aluno\n [2]Lista de alunos cadastrados\n [3]Buscar aluno\n [4]Remover Aluno\n [5]Atualizar o nome do Aluno\n [6]Salvar Arquivo\n [0]Sair ") 
    opt= int (input ("Escolha uma opção:")) 
    return opt 
 
def add (): 
    aluno=str (input ("Digite o nome do Aluno:")) 
    if aluno in laluno: 
        print ("O Aluno já consta na lista!") 
    else: 
        laluno.append (aluno) 
        curso=str (input ("Digite o curso:")) 
        email=str (input ("Digite o email:")) 
        lcurso.append (curso) 
        lemail.append (email) 
        print ("Aluno cadastrado com sucesso!") 
    pass 
 
def ver_td (): 
    print (todos) 
    pass 
 
def pesquisa (): 
    aluno=str (input ("Digite o nome do aluno:")) 
    if aluno in laluno: 
        print (laluno) 
    else: 
        print ("O nome não se encontra na lista. Tente novamente!") 
    pass 
 
def remover (): 
    aluno=str (input ("Digite o nome do aluno:")) 
    if aluno in laluno: 
        laluno.remove (aluno) 
        print ("Aluno removido com sucesso!") 
    else: 
        print ("Aluno não encontrado. Tente novamente!") 
    pass 
 
def edit (): 
    aluno=str (input ("Digite o nome do Aluno que deseja alterar:")) 
    if aluno in laluno: 
        laluno.remove (aluno) 
        aluno=str (input ("Digite o nome do novo aluno")) 
        laluno.append (aluno) 
        ask=str (input ("Deseja alterar Curso e Email Também? [S/N]")) 
        if ask == "Ss": 
            curso=str (input ("Digite o nome do curso que deseja alterar:")) 
            lcurso.remove (curso) 
            curso=str (input ("Digite o nome do novo curso:")) 
            lcurso.append (curso) 
            email=str (input ("Digite o email que deseja alterar:")) 
            lemail.remove (email) 
            email=str (input ("Digite um novo email")) 
            lemail.append (email) 
            print ("Alterações feitas com sucesso") 
        else: 
            print ("Nome alterado com sucesso!") 
             
def salvar ():  
    save=str(input("Deseja salvar arquivo? [S/N]"))  
    if save=="Ss":  
        arquivoName=str(input("Digite o nome do arquivo:"))  
        for i in arquivoName:  
            arquivo=open(arquivoName,"w")  
            arquivo.write(str(i))  
            arquivo.close()  
    else:  
        print("Obrigado por utilizar nosso sistema!")  
pass  
 
opcao = menu ()  
 
while True: 
  if opcao == "1": 
      add () 
  elif opcao == "2": 
      ver_td () 
  elif opcao == "3": 
      pesquisa () 
  elif opcao == "4": 
      remover () 
  elif opcao == "5": 
      edit () 
  elif opcao == "6": 
      salvar () 
  elif opcao == "0": 
      print("Obrigado por utilizar um de nossos serviços.") 
      break
