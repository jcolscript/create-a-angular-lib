# Criando uma LIB angular

## Começando

1. Para criar a pasta para colocar a lib rode o seguinte comando `ng new project-name --create-aplication=false`, dessa forma teremos um projeto angular vazio (sem estrutura).

2. Entre na pasta que foi criada no passo anterior e rode o seguinte comando `ng g library @pan-example/lib-example` para criar em si.

3. Modifique e adicione da forma que vc desejar, mas nao esqueça de organizar o arquivo `project-name/projects/pan-example/src/lib/lib-example.module.ts` corretamente com seus respectivos exports. Faça o mesmo com o arquivo public-api, organize as referencias.

4. Para testar a lib que vc esta desenvolvendo, crie uma aplicacão dentro do seu projeto com o seguinte comando `ng g aplication example-app`. Ele criará a aplicação no diretorio projects/exempla-app.

5. Para que o build da lib seja executado a cada modificação basta rodar o comando `npm run watch`.

6. E agora para rodar a aplição que vc criou para testar a sua lib rode o comando `npm start`.

7. Para adicionar a lib criada no projeto de examplo basta importar o modulo da lib no seu app.module.ts, o import deve ficar parecido com `import { LibExampleModule } from @pan-example/lib-example`. Com isso vc ja pode utilizar as tags dos componentes criados na lib.

## Publicando

1. Na raiz do projeto rode o comando `ng build --prod` para compilar a aplicação.

2. Acesse o diretorio `dist/pan-example/lib-example` e use o comando `npm login` para logar no npm.

2. Apos logar rode o comando `npm publish`, ele ira compilar e tentar enviar o pacote para o npm. Note que dara um erro, isso ocorre por que estamos usando o @pan-example e ele entende que se torna de uma dependencia privada e solicita pagamento.

3. Para tornar sua lib publica no npm rode o comando `npm publish --access public` indicando que sua lib será publica.

