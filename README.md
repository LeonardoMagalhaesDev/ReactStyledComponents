STYLE CONPONENTS
 site => https://styled-components.com/

DOW => npm install --save styled-components


import styled from 'styled-components';

EX: 
	const Botao = styled.button`
    		background-color: #3f51b5;
    		color: white;
    		padding: 10px;
    		border: none;
	`;
------------------------------------------

import { createGlobalStyle } from "styled-components";

EX:
const GlobalStyle = createGlobalStyle`
* {
    box-sizing: border-box;
    font-family: "Montserrat", sans-serif;
    margin: 0;
    padding: 0;
    text-decoration: none;
    color: grey;
  }

----------------------------------------
Utilizando Props

EX:
	background: ${(props) => (props.primary ? "white" : corPrimaria)};
  	color: ${(props) => (props.primary ? corPrimaria : "white")};

	<BtnCabecalho primary href="https://google.com">
          Ajuda
      </BtnCabecalho>
      <BtnCabecalho href="https://google.com">
          Sair
      </BtnCabecalho>
---------------------------------------------------

HERDANDO Icone para IconeMargin 

// MY CONPONENTS
import { Icone } from "../UI";

// MY STYLED-COMPONENTS
import styled from "styled-components";

EX:
	const IconeMargin = styled(Icone)`
  	 margin-top:2px;
	`

	<IconeMargin
          src={toggleState ? privado : olho_icone}
          alt="Privacidade do Saldo"
        />
----------------------------------------------


import { ThemeProvider } from 'styled-components'
import { temaClaro, temaEscuro} from './Components/UI/temas' 

EX:
return (
    <ThemeProvider theme={temaEscuro}>
      <GlobalStyle />
      <Cabecalho />
      <Container />
    </ThemeProvider>
  );

background-color: ${({theme}) => theme.body};
