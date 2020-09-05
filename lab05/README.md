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
  
  randSmyle() {
       let caracter = [':D', ':P', ':-)', '=)', 'q=)', ':~)'];
       let rand = Math.floor(Math.random() * (6 - 0)) + 0;
       return caracter[rand];
  }
}

const elemento = <div>
                   <h2>O dinossauro</h2>                    
                   <h2>pulou na lama.</h2>
                   <div id="smyle"></div>
                 </div>
ReactDOM.render(elemento, 
        document.getElementById("root"));

function showSmyle() {
  const smyle = (
    <div>
      <h1>{new Barra().randSmyle()}</h1>
    </div>
  );
  ReactDOM.render(smyle, document.getElementById('smyle'));
} setInterval(showSmyle, 800);
~~~
