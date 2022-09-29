# Modelagem do Banco de Dados
Repositório para modelagem do banco de dados

<div align="center">
  <img src="https://github.com/MikaelDiogo/README.md-/blob/main/provbdlogico2.png?raw=true"/>
</div>

# Descrição das tabelas do modelo

<h2>Tabela <i>historico</i></h2>

<ul>
  <p>A tabela histórico descreve dentro no modelo relacional elaborado, onde e quais atributos iremos manter no banco sobre nosso sistema. Nela possuímos os atributos/colunas: </p>
    <p>frequencia:Faz referência a presença de um aluno em específico.
    <p>nota:Faz referência a nota das avaliações de um aluno em específico.</p>
    <p>ano:chave primária da tabela, faz referência ao ano em que a turma está estudando</p>
    <p>cod_turma:Chave primária da tabela, faz referência ao código específico de cada turma.</p>
    <p>cod_disc:chave primária da tabela, faz referência ao código específico de cada disciplina</p>
    <p>mat:chave estrangeira da tabela, referência as matérias.</p>
    <p>cod_prof:chave primária da tabela, faz referência ao código específico de cada professor.</p>
    <p>Obs:A tabela histórico tem uma chave primária composta, que vêm dos dados das outras tabelas.</p>    
    </p>
    <br>
</ul>

<h2>Tabela <i>Turma</i></h2>
A tabela <i>turma</i> será na nossa base de dados a responsável por manter os dados das turmas do sistema.
Nela possuímos os atributos/colunas:
<ul>
   <p>cod_disc:referência o código de uma disciplina em específico.</p>
    <p>cod_turma:chave primária da tabela.</p>
    <p>cod_prof:faz referência ao código específico de cada professor.</p>
    <p>ano:chave primária da tabela</p>
    <p>horario:quantidade de horas juntando as aulas.</p>
</ul>

<h2>Tabela <i>ensina</i></h2>
Tabela <i>ensina</i> , é uma tabela de ligação entre as tabelas turma e professores. Nela possuímos os atributos/colunas:
<ul>
  <p>fk_professores_cod_prof:chave estrangeira que faz referência a tabela professores.</p>
    <p>fk_turma_cod_turma:chave estrangeira que faz referência a tabela turma.</p>
    <p>fk_turma_ano: chave estrangeira que faz referência a tabela turma.</p>
 </ul>
 
<h2>Tabela <i>professores</i></h2>
Tabela <i>professores</i> será na nossa base de dados a responsável por manter os dados dos professores do sistema.
Nela possuímos os atributos/colunas:

<ul>
  <p>cod_prof:chave primária da tabela.</p>
    <p>nome_prof:nome do professor</p>
    <p>endereco_prof:endereço do professor.</p>
    <p>cidade_prof:cidade em que o professor nasceu.</p>
</ul>

<h2>Tabela <i>tem</i></h2>
Tabela <i>tem</i> é uma tabela de ligação entre as tabelas disciplinas e professores. Nela possuímos os atributos/colunas:
<ul>
   <p>fk_disciplinas_cod_disc:chave estrangeira que faz referência a tabela disciplinas.</p>
    <p>fk_professores_cod_prof:chave estrangeira que faz referência a tabela professores. </p> 
   
</ul>

<h2>Tabela <i>disciplinas</i></h2>
Tabela <i>disciplinas</i> será na nossa base de dados a responsável por manter os dados das disciplinas do sistema.
Nela possuímos os atributos/colunas:
<ul>
  <p>cod_disc:chave primária da tabela.</p>
    <p>nome_disc:Nome da disciplina.</p>
    <p>carga_hor:É a carga horária das aulas.</p>
</ul>

<h2>Tabela <i>estuda</i></h2>
Tabela <i>estuda</i> é uma tabela de ligação entre as tabelas disciplinas e alunos. Nela possuímos os atributos/colunas:
<ul>
    <p>fk_alunos_mat:chave estrangeira que faz referência a tabela alunos.</p>
    <p>fk_disciplinas_cod_disc:chave estrangeira que faz referência a tabela disciplinas.</p>
</ul>

<h2>Tabela <i>alunos</i></h2>
Tabela <i>alunos</i> será na nossa base de dados a responsável por manter os dados dos alunos do sistema.
Nela possuímos os atributos/colunas:
<ul>
  <p>mat:chave primária da tabela.</p>
    <p>nome:nome do aluno específico.</p>
    <p>endereco:endereço do aluno específico.</p>
    <p>cidade:cidade em que o aluno nasceu.</p>
</ul>
