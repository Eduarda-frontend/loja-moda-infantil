# Loja Moda Infantil 👗👶

Este é o código-fonte de uma loja online de moda infantil! O site foi feito usando HTML, CSS, JavaScript e Bootstrap. Ele é super interativo e responsivo, com várias funcionalidades legais para facilitar a navegação e a experiência do usuário. 🛍️

🚧 ATENÇÃO: Este projeto ainda está em desenvolvimento! 🚧

Ainda estamos trabalhando nas funcionalidades e ajustes finais, então fique à vontade para explorar, mas tenha em mente que algumas partes podem não estar 100% prontas ainda. 😉

## Funcionalidades 🚀

- **Menu de navegação**: O menu tem as categorias "Meninas", "Meninos", "Categorias" e também links para "Sobre Nós", "Pronta Entrega", "FAQ" e "Fale Conosco". 🔍
- **Carrossel de imagens**: Um carrossel de imagens que passa automaticamente, perfeito para mostrar promoções e novidades. 📸
- **Produtos e Tamanhos**: Exibe produtos de várias categorias com informações sobre tamanhos e preços. 👕
- **Formulário de contato**: Um formulário com validação em tempo real para enviar mensagens para a loja. ✉️
- **Máscara para telefone**: O campo de telefone é automaticamente formatado para o padrão `(00) 00000-0000`. 📞
- **Modal de alerta**: Um modal que aparece depois de 3 segundos, avisando que o site ainda está em desenvolvimento. ⚠️
- **ScrollSpy**: O menu de navegação destaca a seção ativa conforme você vai rolando a página. 📰

## Funcionalidades Técnicas (JavaScript) 💻

O projeto tem várias funcionalidades bacanas feitas com JavaScript:

- **ScrollSpy**: 
  - O `scrollspy` é usado para atualizar o menu conforme o usuário rola pela página, assim você sempre sabe em que parte do site está. 
  ```javascript
  $('body').scrollspy({ target: '#cabecalho', offset: 10 });
  ```

- **Máscara de telefone**:
  - A máscara `(00) 00000-0000` é aplicada automaticamente no campo de telefone com a ajuda do `jQuery Mask`. 
  ```javascript
  $('#telefone').mask('(00) 00000-0000', {
    placeholder: '(00) 00000-00000'
  });
  ```

- **Validação do formulário**:
  - O formulário verifica se os campos estão preenchidos corretamente (nome, e-mail, mensagem) usando o `jQuery Validate`. 
  ```javascript
  $('form').validate({
    rules: {
      nome: { required: true },
      email: { required: true, email: true },
      mensagem: { required: true }
    },
    messages: {
      nome: 'Por favor, insira o seu nome!'
    },
    submitHandler: function (form) {
      console.log(form);  // Aqui você pode adicionar a lógica de envio do formulário
    },
    invalidHandler: function (evento, validador) {
      let camposIncorretos = validador.numberOfInvalids();
      if (camposIncorretos) {
        alert(`Existem ${camposIncorretos} campos incorretos!`);
      }
    }
  });
  ```

- **Exibição de modal**:
  - Um modal aparece automaticamente após 3 segundos para informar que o site ainda está em desenvolvimento. 
  ```javascript
  document.addEventListener('DOMContentLoaded', function() {
    const modal = new bootstrap.Modal('#modal');
    setTimeout(function() {
      modal.show();
    }, 3000);
  });
  ```

## Estrutura do Projeto 📁

Aqui estão os principais arquivos e tecnologias usados:

- **HTML**: Estrutura básica do site, incluindo o menu, seções de produtos e o formulário de contato.
- **CSS**: Estilos customizados, além do Bootstrap para garantir que o site fique responsivo. 🎨
- **JavaScript/jQuery**: Para tornar tudo interativo, como validação de formulários, mascaramento de campos e controle de eventos.
- **Bibliotecas**:
  - Bootstrap (para os componentes responsivos e bonitos como o menu e o carrossel) ⚙️
  - jQuery (para facilitar a manipulação do DOM e validação) 
  - jQuery Mask (para as máscaras de campo de telefone)
  - jQuery Validate (para garantir que os campos do formulário sejam preenchidos corretamente)


## Como Contribuir 🤗

Se quiser ajudar a melhorar o projeto, você pode:

- Fazer melhorias no código.
- Reportar bugs ou erros.
- Sugerir novas funcionalidades.

Espero que curta a loja e, se precisar, é só entrar em contato pelo WhatsApp! 📲

---
