



# React Router Dom

## 🌐 O que é o React Router Dom?

O React Router Dom é uma poderosa biblioteca do React que tem como principal objetivo facilitar a manipulação de rotas em aplicações SPA (Single-Page Application). Ao invés de recarregar a página inteira, ele permite que diferentes componentes sejam renderizados em uma única página conforme a rota acessada, tornando a navegação mais fluida e eficiente.

Essa biblioteca é especialmente útil para criar caminhos específicos no seu site, permitindo o acesso e a renderização de diferentes componentes sem a necessidade de sair do ambiente atual.

## 🛠 Como ele funciona?

O princípio por trás do React Router Dom está ligado ao conceito de SPA. Em uma SPA, uma única página carrega todos os componentes necessários. Assim, ao invés de fazer novas requisições ao servidor cada vez que um link é clicado, a aplicação simplesmente renderiza o componente correspondente à rota acessada.

O React Router Dom age como um "intermediário", escutando a URL atual e decidindo qual componente deve ser mostrado, tudo isso sem a necessidade de recarregar a página.

**Exemplos de aplicações famosas construídas como SPAs**:

- Facebook
- Instagram
- Netflix
- Dropbox

O React Router Dom torna esse processo ainda mais intuitivo e eficaz em aplicações React, proporcionando uma experiência de usuário mais ágil e responsiva.

## Como utilizar React Router Dom

O React Router Dom é composto por quatro principais elementos: `BrowserRouter`, `Routes`, `Route` e `Link`.

### BrowserRouter

- `BrowserRouter` é responsável por interagir com os nós do DOM, especificamente com `History` e `Location`. Ele já fornece configurações prontas da própria biblioteca para o React Router Dom funcionar. **Importante:** deve sempre envolver todos os outros elementos da biblioteca.

### Routes

- `Routes` é o container que guarda todas as rotas definidas. As rotas individuais são criadas dentro deste componente.

### Route 

- `Route` é onde definimos os caminhos para os nossos componentes. Importamos os componentes desejados e os especificamos dentro de `Route` usando a propriedade `element`, por exemplo: `element={<Inicio/>}`. O atributo `path` define o caminho para esse componente, como `path="/inicio"`.

### Link

- `Link` é utilizado para criar links de navegação entre as rotas. Ele se conecta à `Route` por meio do atributo `to`. Por exemplo, `to="/inicio"` cria um link que direcionará o usuário para o componente definido em `Route` com `path="/inicio"`.

# Exemplo

```javascript
import Inicio from "./Components/Inicio.js"
import {BrowserRouter, Routes, Route, Link} from "react-router-dom";

export default function App(){
    return(
        <BrowserRouter >
            <nav>
                <ul>
                    <li><Link to="/">Inicio</Link><li>
                </ul>
            </nav>
            <Routes>
                <Route path="/" element={<Inicio/>}>
            </Routes>
        </BrowserRouter>
    )
}
```

<br/>
<a href="https://codesandbox.io/s/goofy-violet-nxrkw6?file=/src/App.js">Código da aula CodeSandBox</a>