# Banco-de-dados-Asecab-
Banco de Dados(PostgreSQI) - ASECAB
CREATE TABLE "Informações - Extra" (
  "0001" <type>,
  "Período do curso" <type>,
  "" <type>,
  "Manhã" <type>,
  "Tarde" <type>,
  "A criança virá sozinha?" <type>,
  "Acompanhada por quem?" <type>,
  "" <type>,
  PRIMARY KEY ("0001"),
  CONSTRAINT "FK_Informações - Extra.A criança virá sozinha?"
    FOREIGN KEY ("A criança virá sozinha?")
      REFERENCES "Dados Pessoais"("Nome do pai"),
  CONSTRAINT "FK_Informações - Extra.0001"
    FOREIGN KEY ("0001")
      REFERENCES "Dados Pessoais"("0001")
);

CREATE TABLE "Dados dos responsáveis" (
  "" <type>,
  "0001" <type>,
  "1º Reponsável Legal" <type>,
  "Nome" <type>,
  "Data de Nascimento" <type>,
  "Telefone" <type>,
  "Telefone" <type>,
  "Grau de parentesco" <type>,
  "2º Responsável Legal" <type>,
  "Data de Nascimento" <type>,
  "1º Telefone" <type>,
  "2º Telefone" <type>,
  "Grau de parentesco" <type>,
  PRIMARY KEY ("0001"),
  CONSTRAINT "FK_Dados dos responsáveis.Nome"
    FOREIGN KEY ("Nome")
      REFERENCES "Informações - Extra"("A criança virá sozinha?"),
  CONSTRAINT "FK_Dados dos responsáveis.0001"
    FOREIGN KEY ("0001")
      REFERENCES "Informações - Extra"("0001")
);

CREATE TABLE "Acompanhamento médico / Informações sobre saúde" (
  "" <type>,
  "0001" <type>,
  "UBS de referência" <type>,
  "Toma algum medicamento controlado?" <type>,
  "Possui algum problema de saúde que requer acompanhamento médico?" <type>,
  "Qual?" <type>,
  "Possui alguma restrição alimentar?" <type>,
  "Possui alguma restrição a atividade física?" <type>,
  "Têm bronquite?" <type>,
  "Têm asma?" <type>,
  "Têm alguma alergia?" <type>,
  "Possui alguma deficiência física?" <type>,
  "Observações:" <type>,
  PRIMARY KEY ("0001"),
  CONSTRAINT "FK_Acompanhamento médico / Informações sobre saúde.0001"
    FOREIGN KEY ("0001")
      REFERENCES "Dados dos responsáveis"("0001"),
  CONSTRAINT "FK_Acompanhamento médico / Informações sobre saúde.UBS de referência"
    FOREIGN KEY ("UBS de referência")
      REFERENCES "Dados dos responsáveis"("Nome")
);

CREATE TABLE "Situação escolar" (
  "" <type>,
  "0001" <type>,
  "Está matriculado?" <type>,
  "Escola" <type>,
  "Série" <type>,
  "Período" <type>,
  "Parou de frequentar a escola?" <type>,
  "Motivo" <type>,
  "Por quanto tempo?" <type>,
  PRIMARY KEY ("0001"),
  CONSTRAINT "FK_Situação escolar.0001"
    FOREIGN KEY ("0001")
      REFERENCES "Acompanhamento médico / Informações sobre saúde"("0001")
);

