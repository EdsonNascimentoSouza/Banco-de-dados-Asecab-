# Banco-de-dados-Asecab-
Projeto de automatização e/ou digitalização de arquivos da instituição não governamental ASECAB.
Modelagem gerado no Site Lucidchart.

CREATE TABLE `Cadastro` (
  `Nº` Nome,
  `0001` <type>,
  `` <type>,
  `` <type>,
  PRIMARY KEY (`0001`)
);

CREATE TABLE `Dados Pessoais` (
  `0001` <type>,
  `Data de Nascimento` <type>,
  `Naturalidade` <type>,
  `Raça/Cor` <type>,
  `RG` <type>,
  `CPF` <type>,
  `Endereço` <type>,
  `Nome do pai` <type>,
  `Nome da mãe` <type>,
  PRIMARY KEY (`0001`),
  FOREIGN KEY (`0001`) REFERENCES `Cadastro`(`0001`)
);

CREATE TABLE `Dados dos responsáveis` (
  `` <type>,
  `0001` <type>,
  `1º Reponsável Legal` <type>,
  `Nome` <type>,
  `Data de Nascimento` <type>,
  `Telefone` <type>,
  `Telefone` <type>,
  `Grau de parentesco` <type>,
  `2º Responsável Legal` <type>,
  `Data de Nascimento` <type>,
  `1º Telefone` <type>,
  `2º Telefone` <type>,
  `Grau de parentesco` <type>,
  PRIMARY KEY (`0001`)
);



