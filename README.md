# Atomic-design
Projeto senai
Aqui está um exemplo de código que demonstra a implementação do Atomic Design em React:

Átomos
- Button.js
import React from 'react';

const Button = ({ children, onClick }) => {
  return (
    <button onClick={onClick}>
      {children}
    </button>
  );
};

export default Button;

- Input.js
import React from 'react';

const Input = ({ type, placeholder, value, onChange }) => {
  return (
    <input type={type} placeholder={placeholder} value={value} onChange={onChange} />
  );
};

export default Input;

Moléculas
- Form.js
import React from 'react';
import Button from './Button';
import Input from './Input';

const Form = ({ onSubmit }) => {
  return (
    <form onSubmit={onSubmit}>
      <Input type="text" placeholder="Nome" />
      <Input type="email" placeholder="E-mail" />
      <Button type="submit">Enviar</Button>
    </form>
  );
};

export default Form;

Organismos
- Header.js
import React from 'react';
import Form from './Form';

const Header = () => {
  return (
    <header>
      <h1>Meu App</h1>
      <Form />
    </header>
  );
};

export default Header;

Templates
- Layout.js
import React from 'react';
import Header from './Header';

const Layout = ({ children }) => {
  return (
    <div>
      <Header />
      <main>
        {children}
      </main>
    </div>
  );
};

export default Layout;

Páginas
- Home.js
import React from 'react';
import Layout from './Layout';

const Home = () => {
  return (
    <Layout>
      <h2>Bem-vindo ao meu app!</h2>
    </Layout>
  );
};

export default Home;

Esse exemplo demonstra como criar componentes atômicos e combiná-los para formar componentes mais complexos, seguindo a estrutura do Atomic Design.
