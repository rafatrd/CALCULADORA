
    </style>
</head>
<body>
    <div class="fundo">
        <h1>RAFAEL S S MARQUES</h1>
        <div class="calculadora">
        <h1>calculadora</h1>
       <p id="resultado"> </p>
       <table>
        <tr>
            <td><button class="botao" onclick="clean()">C</button></td>
            <td><button class="botao" onclick="back()"><</button></td>
            <td><button class="botao" onclick="insert('/')">/</button></td>
            <td><button class="botao" onclick="insert('*')">X</button></td>
        </tr>
        <tr>
            <td><button class="botao" onclick="insert('7')">7</button></td>
            <td><button class="botao" onclick="insert('8')">8</button></td>
            <td><button class="botao" onclick="insert('9')">9</button></td>
            <td><button class="botao" onclick="insert('-')">-</button></td>
        </tr>
        <tr>
            <td><button class="botao" onclick="insert('4')">4</button></td>
            <td><button class="botao" onclick="insert('5')">5</button></td>
            <td><button class="botao" onclick="insert('6')">6</button></td>
            <td><button class="botao" onclick="insert('+')">+</button></td>
        </tr>
        <tr>
            <td><button class="botao" onclick="insert('1')">1</button></td>
            <td><button class="botao" onclick="insert('2')">2</button></td>
            <td><button class="botao" onclick="insert('3')">3</button></td>
            <td rowspan="2"><button class="botao" style="height: 106px;" onclick="calcular()">=</button></td>
        </tr>
        <tr>
            <td colspan="2"><button class="botao" style="width: 106px;" onclick="insert('0')">0</button></td>
            <td><button class="botao" onclick="insert('.')">.</button></td>
        </tr>
    </table>
</div>
</div>
<script>
function insert(num)
{
    var numero = document.getElementById('resultado').innerHTML;
    document.getElementById('resultado').innerHTML = numero + num;
}
function clean()
{
    document.getElementById('resultado').innerHTML = "";
}
function back()
{
    var resultado = document.getElementById('resultado').innerHTML;
    document.getElementById('resultado').innerHTML = resultado.substring(0, resultado.length -1);
}
function calcular()
{
    var resultado = document.getElementById('resultado').innerHTML;
    if(resultado)
    {
        document.getElementById('resultado').innerHTML = eval(resultado);
    }
    else
    {
        document.getElementById('resultado').innerHTML = "Nada..."
    }
}
</script>
</body>
</html>
