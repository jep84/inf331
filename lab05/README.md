## Tarefa 1

![Diagrama de Subcomponentes](images/tarefa1.png)

## Tarefa 2

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
}

const elemento = <div>
                   <h2>O dinossauro</h2>
                   <Barra tamanho="10"/>
                   <h2>pulou na lama.</h2>
                 </div>
ReactDOM.render(elemento, 
        document.getElementById("root"));
~~~
