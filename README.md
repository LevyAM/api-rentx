# Cadastro de Carro

**RF** => REQUISITOS FUNCIONAIS
Deve ser possível cadastrar um novo carro.
Deve ser possível listar todas as categorias.

**RN** => REGRAS DE NEGÓCIO
Não deve ser possível cadastrar um carro com uma placa já existente.
O carro deve ser cadastrado, por padrão, com disponibilidade.
* O usuário responsável pelo cadastro deve ser um administrador.

# Listagem de carros

**RF** => REQUISITOS FUNCIONAIS
Deve ser possível listar todos os carros disponíveis.
Deve ser possível listar todos os carros disponíveis pelo nome da categoria.
Deve ser possível listar todos os carros disponíveis pelo nome da marca.
Deve ser possível listar todos os carros disponíveis pelo nome do carro.

**RN** => REGRAS DE NEGÓCIO
O usuário não precisa estar logado no sistema.

# Cadastro de Especificação do Carro

**RF** => REQUISITOS FUNCIONAIS
Deve ser possível cadastrar uma especificação para um carro.
Deve ser possível listar todas as especificações.
Deve ser possível listar todos os carros.

**RN** => REGRAS DE NEGÓCIO
Não deve ser possível cadastrar uma especificação para um carro não cadastrado.
Não deve ser possível cadastrar uma especificação já existente para o mesmo carro.
O usuário responsável pelo cadastro deve ser um administrador.

# Cadastro de Imagens do Carro

**RF** => REQUISITOS FUNCIONAIS
Deve ser possível cadastrar as imagens do carro.

**RNF** => REQUISITOS NÃO-FUNCIONAIS
Utilizar o multer para upload dos arquivos.

**RN** => REGRAS DE NEGÓCIO
O usuário deve poder cadastrar mais de uma imagem para o mesmo carro.
O usuário responsável pelo cadastro deve ser um usuário administrador.

# Aluguel de Carros

**RF** => REQUISITOS FUNCIONAIS
Deve ser possível cadastrar um aluguel.

**RN** => REGRAS DE NEGÓCIO
O aluguel deve ter duração mínima de 24 horas.
Não deve ser possível cadastrar um novo aluguel caso já exista um aberto para o mesmo usuário.
Não deve ser possível cadastrar um novo aluguel caso já exista um aberto para o mesmo carro.
O usuário deve estar logado na aplicação.
Ao realizar um aluguel, o status do carro deverá ser alterado paras indiponível.

# Devolução de carro

**RF** => REQUISITOS FUNCIONAIS
Deve ser possível realizar a devolução de um carro.

**RN** => REGRAS DE NEGÓCIO
Se o carro for devolvido em menos de 24 horas, deverá ser cobrado diária completa.
Ao realizar a devolução, o carro deverá ser liberado para outro aluguel.
Ao realizar a devolução, o usuário deverá ser liberado para outro aluguel.
Ao realizar a devolução, deverá ser calculado o total do aluguel.
Caso o horário de devolução seja superior ao horário previsto de entrega, deverá ser cobrada multa proporcional aos dias de atraso.
Caso haja multa, deverá ser somado ao total do aluguel.
O usuário deve estar logado na aplicação.

# Listagem de Alugueis para usuário

**RF** => REQUISITOS FUNCIONAIS
Deve ser possível realizar a busca de todos os alugueis de um usuário

**RN** => REGRAS DE NEGÓCIO
O usuário deve estar logado na aplicação.

#Recuperar Senha

**RF** => REQUISITOS FUNCIONAIS
Deve ser possível o usuário recuperar a senha informando o email.
O usuário deve receber um email com o passo-a-passo para a recuperação da senha.
O usuário deve conseguir inserir uma nova senha.

**RN** => REGRAS DE NEGÓCIO
O usuário precisa informar uma nova senha.
O link enviado para a recuperação deve expirar em 3 horas.