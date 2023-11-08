# BANCO-DE-DADOS
Atividade Aula banco de dados 

De acordo com os conceitos estudados, exiba os resultados das consultas das operações select, project, união, intersecção e diferença. Siga as instruções com base na tabela apresentada em anexo.

- Mostre as informações apenas dos alunos aprovados. A aprovação é acima de 7,0;
- Exiba as informações dos alunos do primeiro ano com nota maior ou igual a 8,0;
- Exiba apenas os nomes e as notas dos alunos;
- Crie uma tabela PROFESSOR que apresente apenas o primeiro e o último nome do professor;
- Crie uma tabela ALUNO com o primeiro e o último nome de cada;
- Mostre o resultado da união entre a tabela ALUNO(PNome, UNome) e a tabela PROFESSOR;
- Exiba o resultado da intersecção entre a tabela ALUNO(PNome, UNome) e a tabela PROFESSOR;
- Exiba o resultado da diferença entre a tabela ALUNO(PNome, UNome) e a tabela PROFESSOR.



SELECT * FROM ALUNO WHERE Nota > 7.0;
SELECT * FROM ALUNO WHERE Ano = 'Primeiro' AND Nota >= 8.0;
SELECT Nome, Nota FROM ALUNO;
CREATE TABLE PROFESSOR (
  Primeiro_Nome VARCHAR(50),
  Ultimo_Nome VARCHAR(50)
);
CREATE TABLE ALUNO (
  Primeiro_Nome VARCHAR(50),
  Ultimo_Nome VARCHAR(50)
);
SELECT Primeiro_Nome, Ultimo_Nome FROM ALUNO
UNION
SELECT Primeiro_Nome, Ultimo_Nome FROM PROFESSOR;
SELECT Primeiro_Nome, Ultimo_Nome FROM ALUNO
INTERSECT
SELECT Primeiro_Nome, Ultimo_Nome FROM PROFESSOR;
(SELECT Primeiro_Nome, Ultimo_Nome FROM ALUNO)
EXCEPT
(SELECT Primeiro_Nome, Ultimo_Nome FROM PROFESSOR);


