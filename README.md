# Sistema de Gestão Hoteleira
## Índice
- [Configuração](#setup)
- [Capturas de tela](#capturas de tela)
- [Para desenvolvedor](#para-desenvolvedor)

## Configurar
1. Certifique-se de ter `MySQL` e um servidor web para executar/interpretar `PHP` em seu sistema.
2. Clone ou baixe o repositório e coloque-o em `xampp/htdocs/` se você estiver usando Windows, caso contrário, verifique o(s) tutorial(s) para seu servidor web e sistema operacional correspondente.
3. Instale dependências para JavaScript, `npm install` e PHP, `composer install`.
4. Crie um banco de dados chamado `hotel` e execute o script [`hotel.sql`](https://github.com/tramyardg/hotel-mgmt-system/blob/master/hotel.sql) para criar tabelas e preencher dados. Certifique-se de que sua configuração corresponda a [`app/DB.php`](https://github.com/tramyardg/hotel-mgmt-system/blob/master/app/DB.php#L14), caso contrário, faça as alterações desejadas .
5. Execute o aplicativo.

## Crie a sua conta aqui
1. Vá para a página de registro (register.php), ou seja, http://hotel.local/register.php
2. Insira suas informações.
3. Para criar uma conta de administrador
   - 3.1 acesse o banco de dados do seu hotel
   - 3.2 selecionar cliente da mesa
   - 3.3 selecione uma conta
   - 3.4 altere o valor de isadmin para 1
 

## Capturas de tela
**Cliente**
- Preço do quarto
![room_pricing](https://user-images.githubusercontent.com/5623994/51089111-f0131a00-1735-11e9-8758-847091e9b68e.PNG)
- Ficha de reserva
![formulário_reserva](https://user-images.githubusercontent.com/5623994/51089124-218be580-1736-11e9-9400-3cfd5454fe56.PNG)
- Ver reservas
![view_booking](https://user-images.githubusercontent.com/5623994/51089133-38cad300-1736-11e9-857a-64f9956b9f17.PNG)
- Sobre o usuário
![about_user](https://user-images.githubusercontent.com/5623994/51089140-4f712a00-1736-11e9-850f-6bb67151711e.PNG)

**Administrador**
- Gerenciar reservas
![manage_booking](https://user-images.githubusercontent.com/5623994/51089150-6d3e8f00-1736-11e9-9af0-601ef58847b4.PNG)

## Para desenvolvedor
**Execute testes de unidade PHP**
```
$ ./vendor/bin/phpunit testes
```
```
$ ./vendor/bin/phpunit testes/CustomerHandlerTest.php
```
```
$ ./vendor/bin/phpunit --filter testUpdateTestes de clientes
```
**Execute o embelezador e fixador de código PHP**
```
$ ./vendor/bin/phpcbf app/process_login.php --standard=ruleset.xml
```
```
$ ./vendor/bin/phpcbf app/*/*.php --standard=ruleset.xml
```
**Execute ESLint para formatar/corrigir código JavaScript**
```
npm executa eslint
```
```
npm executa eslint -- --fix
```
