
# <font color=#671402> JUPYTER
</font>


En este curso usaremos la poderosísima herramienta de jupyter. Para iniciar jupyter, debemos simplemente teclear en la terminal lo siguiente: 
       
       jupyter notebook 

Algunos comandos útiles de teclado son: 

- Ctrl-m m: marcar la celda a *markdown*
- Ctrl-m y: marcar la celda a *code* 

<div style="background-color: #E8DAEF; padding: 15px;"> <b>NOTA:</b> Markdown soporta toda clase de código en latex que no requiera de un paquete tecleando simplemente <span>$</span> o <span>$$</span>:</div>

Ejemplo:

$$
\nabla \cdot E = \frac{\rho}{\epsilon_0}
$$

# <font color=#671402> LO MUY BÁSICO DE PYTHON
</font>

## Sentencia Print 
Como ya sabrás, para que python imprima lo que uno quiera se utiliza `print()`. Esto es compatible con Python 2 y 3. *En python 2 no es necesario el paréntesis, pero en python 3 sí lo es.* 


```python
x = 'hola pythonistas' #variable tipo str
y = 42                  #variable tipo entero (int)
z = 3.0                #variable tipo decimal (float)
w = 2+2j               #variable tipo compleja (complex)
#python usa la 'j' para denotar la unidad imaginaria
print (x,y,z, w)
```

    ('hola pythonistas', 42, 3.0, (2+2j))


También podemos usar las llaves `{}` para indicar donde van a ir insertadas nuestras variables. Usamos el método `format()` en la cadena para marcar las variables dentro de `{}`. Ejemplo:


```python
print('x = {}, y = {}, z = {}, w = {}'.format(x, y, z, w))
```

    x = hola pythonistas, y = 42, z = 3.0, w = (2+1j)


<div style="background-color: #E8DAEF; padding: 15px;"> <b>NOTA:</b> Para saber el tipo de variable, hacemos $\texttt{type(variable)}$</div>

## Operaciones aritméticas básicas

Las operaciones básicas son `+`, `-`, `*` y `/`. Si realizamos una operación entre un entero y un flotante, el resultado es siempre un flotante. 


```python
print (2+2+3.0) 

print (2+2+3)
```

    7.0
    7


El operador `/` retorna la división y el operador `//` retorna la división entera. 


```python
print 15.0 / 2.0 
print 15.0 // 2.0 
```

    7.5
    7.0


Podemos realizar operaciones sobre la sentencia `print()`. Ejemplo: 



```python
a = 1
b = 2 

print(a+b)
```

    3


También tenemos la operación `%` el cual nos indica el **resto** en un cociente. Ejemplo, al dividir 7/2, el resultado es 3 con resto 1. 


```python
7%2 
```




    1



<div style="background-color: #E8DAEF; padding: 15px;"> <b>NOTA:</b> Una utilidad del módulo se relaciona con los números pares. Por ejemplo, todo número par cumple que n % 2 = 0.</div>

<div style="background-color:#A93226; padding: 10px"><h3><span class="fa fa-flash"></span> EJERCICIO:</h3></div>

Piensa en otra utilidad para la operación `%`


```python
#marca la casilla como markdown 

```

### Operaciones sobre las cadenas 

Existen dos formas para crear un string (cadena). Puedes usar cualquiera de estas dos:


```python
a = 'hola pythonisistas'
b = "como estan"
```

Python nos deja utilizar los operadores de las matemáticas usuales en las cadenas. Esto nos servirá para **unir** o **duplicar** un string. 



```python
print 'union = ',a+b
print 'duplico variable "a" = ', a*2 

```

    union =  hola pythonisistascomo estan
    duplico variable "a" =  hola pythonisistashola pythonisistas


Podemos usar `\n` para crear una nueva linea: 


```python
a = 'holaPython'
b = 'chao'
c = a + '\n' + b 
print c 
```

    holaPython
    chao


### Los booleanos 

Una variable de tipo booleano sólo puede tener dos valores: `True` y `False`. Los booleanos pueden ser creados al **comparar valores**, por ejmplo usando el *operador* `==`,


```python
2 == 3 
```




    False



también pueden ser **asignados** directamente a una variable, por ejemplo: 


```python
variable = True 
print variable
```

    True


<div style="background-color: #E8DAEF; padding: 15px;"> <b>NOTA:</b> Entender este concepto servirá para entender las expresiones condiciones y los bucles.</div>


```python
# preserve
# Esta celda da el estilo al notebook
from IPython.core.display import HTML
css_file = 'styles/aeropython.css'
HTML(open(css_file, "r").read())
```




/* This template is inspired in the one used by Lorena Barba
in the numerical-mooc repository: https://github.com/numerical-mooc/numerical-mooc
We thank her work and hope you also enjoy the look of the notobooks with this style */

<link href='http://fonts.googleapis.com/css?family=Source+Sans+Pro|Josefin+Sans:400,700,400italic|Ubuntu+Condensed' rel='stylesheet' type='text/css'>

El estilo se ha aplicado =)

<style>



#notebook_panel { /* main background */
    background: #f7f7f7;
}

div.cell { /* set cell width */
    width: 900px;
}

div #notebook { /* centre the content */
    background: #fff; /* white background for content */
    width: 950px;
    margin: auto;
    padding-left: 0em;
}

#notebook li { /* More space between bullet points */
    margin-top:0.7em;
}

/* draw border around running cells */
div.cell.border-box-sizing.code_cell.running { 
    border: 1px solid #111;
}

/* Put a solid color box around each cell and its output, visually linking them*/
div.cell.code_cell {
    font-family: 'Source Sans Pro', sans-serif;
    background-color: rgb(256,256,256);
    font-size: 110%;
    border-radius: 0px; 
    padding: 0.5em;
    margin-left:1em;
    margin-top: 1em;
}

div.text_cell_render{
    font-family: 'Josefin Sans', serif;
    line-height: 145%;
    font-size: 125%;
    font-weight: 500;
    width:750px;
    margin-left:auto;
    margin-right:auto;
}


/* Formatting for header cells */
.text_cell_render h1, .text_cell_render h2, .text_cell_render h3,
.text_cell_render h4, .text_cell_render h5 {
    font-family: 'Ubuntu Condensed', sans-serif;
}
/*
.text_cell_render h1 {
    font-family: Flux, 'Ubuntu Condensed', serif;
    font-style:regular;
    font-weight: 400;    
    font-size: 30pt;
    text-align: center;
    line-height: 100%;
    color: #335082;
    margin-bottom: 0.5em;
    margin-top: 0.5em;
    display: block;
}
*/
.text_cell_render h1 {
    font-weight: 600;
    font-size: 35pt;
    line-height: 100%;
    color: #000000;
    margin-bottom: 0.1em;
    margin-top: 0.3em;
    display: block;
}

.text_cell_render h2 {
    margin-top:16px;
    font-size: 27pt;
    font-weight: 550;
    margin-bottom: 0.1em;
    margin-top: 0.3em;
    font-style: regular;
    color: #2c6391;
}	

.text_cell_render h3 {
    font-size: 20pt;
    font-weight: 550
    text-align: left;
    margin-bottom: 0.1em;
    margin-top: 0.3em;
    font-style: regular;
    color:  #387eb8;
}

.text_cell_render h4 {    /*Use this for captions*/
    font-size: 18pt;
    font-weight: 450
    text-align: left;
    margin-bottom: 0.1em;
    margin-top: 0.3em;
    font-style: regular;
    color:  #5797cc;
}

.text_cell_render h5 {  /*Use this for small titles*/
    font-size: 18pt;
    font-weight: 550;
    color: rgb(163,0,0);
    font-style: italic;
    margin-bottom: .1em;
    margin-top: 0.8em;
    display: block;
    color:  #b21c0d;
}

.text_cell_render h6 { /*use this for copyright note*/
    font-family: 'Ubuntu Condensed', sans-serif;
    font-weight: 300;
    font-size: 14pt;
    line-height: 100%;
    color: #252525;
    text-align: right;
    margin-bottom: 1px;
    margin-top: 1px;
}

.CodeMirror{
        font-family: 'Duru Sans', sans-serif;
        font-size: 100%;
}

</style>
<script>
    MathJax.Hub.Config({
                        TeX: {
                           extensions: ["AMSmath.js"],
                           equationNumbers: { autoNumber: "AMS", useLabelIds: true}
                           },
                tex2jax: {
                    inlineMath: [ ['$','$'], ["\\(","\\)"] ],
                    displayMath: [ ['$$','$$'], ["\\[","\\]"] ]
                },
                displayAlign: 'center', // Change this to 'center' to center equations.
                "HTML-CSS": {
                    styles: {'.MathJax_Display': {"margin": 4}}
                }
        });
</script>



