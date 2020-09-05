## Tarefa 1

![Diagrama de Subcomponentes](images/tarefa1.png)

## Tarefa 2
Link para o projeto no Codepen: [React 03 - Componente Barra](https://codepen.io/jep84/pen/poywKym)

**HTML**
~~~html
<div id="root"></div>
~~~

**JavaScript**
~~~javascript
class Barra extends React.Component {
  render() {
    let resultado = "";
    for (let b = 1; b <= this.props.tamanho; b++)
      resultado += "=";
    return resultado;
  }
  
  temperatura() {
       let temperatura = Math.floor(Math.random() * (38 - 30)) + 30;
       let c = "Temperatura: " + temperatura + " °C";
       return c;
  }
  
  umidade() {
       let umidade = Math.floor(Math.random() * (50 - 60)) + 50;
       let c = "Umidade: " + umidade + " %";
       return c;
  }
}

const elemento = <div>
                   <h2>O dinossauro</h2>                          
                   <h2>pulou na lama.</h2>
                   <h3>===============</h3>
                   <h3><u>Condições da Lama</u></h3>
                   <div id="temperatura"></div>
                   <div id="umidade"></div>
                 </div>
ReactDOM.render(elemento, document.getElementById("root"));

function MostraSensores() {
  const temperatura = (
    <div>
      <h3>{new Barra().temperatura()}</h3>
    </div>
  );
  
  const umidade = (
    <div>
      <h3>{new Barra().umidade()}</h3>
    </div>
  );
  
  ReactDOM.render(temperatura, document.getElementById('temperatura'));
  ReactDOM.render(umidade, document.getElementById('umidade'));
  
} setInterval(MostraSensores, 1000);
~~~
