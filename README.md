# Degrades-CSS---FrontEnd
Conteúdo curso Programador Web - Praticas FrontEnd 
 - Planos de fundo Gradientes
 
 Os gradientes CSS permitem exibir transições suaves entre duas ou mais cores especificadas.

CSS define três tipos de gradientes:

Gradientes lineares (desce/cima/esquerda/direita/diagonalmente)
Gradientes radiais (definidos por seu centro)
Gradientes cônicos (girados em torno de um ponto central)
Gradientes Lineares CSS
Para criar um gradiente linear, você deve definir pelo menos duas paradas de cor. Interrupções de cores são as cores entre as quais você deseja renderizar transições suaves. Você também pode definir um ponto inicial e uma direção (ou um ângulo) junto com o efeito de gradiente.

Sintaxe
background-image: linear-gradient(direction, color-stop1, color-stop2, ...);
Direção - De cima para baixo (este é o padrão)

O exemplo a seguir mostra um gradiente linear que começa no topo. Começa vermelho, passando para amarelo:

de cima para baixo (padrão)

Exemplo
#grad {
  background-image: linear-gradient(red, yellow);
}

Direção - Esquerda para Direita

O exemplo a seguir mostra um gradiente linear que começa da esquerda. Começa vermelho, passando para amarelo:

da esquerda para direita

Exemplo
#grad {
  background-image: linear-gradient(to right, red , yellow);
}

Direção - Diagonal

Você pode fazer um gradiente na diagonal especificando as posições iniciais horizontal e vertical.

O exemplo a seguir mostra um gradiente linear que começa no canto superior esquerdo (e vai para o canto inferior direito). Começa vermelho, passando para amarelo:

superior esquerdo para inferior direito

Exemplo
#grad {
  background-image: linear-gradient(to bottom right, red, yellow);
}


Usando Ângulos
Se quiser mais controle sobre a direção do gradiente, você pode definir um ângulo, em vez das direções predefinidas (para baixo, para cima, para a direita, para a esquerda, para baixo à direita, etc.). Um valor de 0deg é equivalente a "to top". Um valor de 90 graus é equivalente a "para a direita". Um valor de 180 graus é equivalente a "to bottom".

Sintaxe
background-image: linear-gradient(angle, color-stop1, color-stop2);
O exemplo a seguir mostra como usar ângulos em gradientes lineares:

180 graus
Exemplo
#grad {
  background-image: linear-gradient(180deg, red, yellow);
}
Usando várias paradas de cores
O exemplo a seguir mostra um gradiente linear (de cima para baixo) com várias paradas de cor:

Exemplo
#grad {
  background-image: linear-gradient(red, yellow, green);
}
O exemplo a seguir mostra como criar um gradiente linear (da esquerda para a direita) com a cor do arco-íris e algum texto:

Fundo do arco-íris
Exemplo
#grad {
  background-image: linear-gradient(to right, red,orange,yellow,green,blue,indigo,violet);
}
Usando Transparência
Os gradientes CSS também oferecem suporte à transparência, que pode ser usada para criar efeitos de esmaecimento.

Para adicionar transparência, usamos a função rgba() para definir as paradas de cor. O último parâmetro na função rgba() pode ser um valor de 0 a 1, e define a transparência da cor: 0 indica transparência total, 1 indica cor total (sem transparência).

O exemplo a seguir mostra um gradiente linear que começa da esquerda. Ele começa totalmente transparente, fazendo a transição para vermelho:

Exemplo
#grad {
  background-image: linear-gradient(to right, rgba(255,0,0,0), rgba(255,0,0,1));
}
Repetindo um gradiente linear
A função repeating-linear-gradient() é usada para repetir gradientes lineares:

Exemplo
Um gradiente linear repetitivo:

#grad {
  background-image: repeating-linear-gradient(red, yellow 10%, green 20%);
}

Gradientes Radiais CSS
Um gradiente radial é definido por seu centro.

Para criar um gradiente radial, você também deve definir pelo menos duas paradas de cor.

Sintaxe
background-image: radial-gradient(shape size at position, start-color, ..., last-color);
Por padrão, a forma é elipse, o tamanho é o canto mais distante e a posição é o centro.

Radial Gradient - Paradas de cor uniformemente espaçadas (este é o padrão)

O exemplo a seguir mostra um gradiente radial com limites de cores uniformemente espaçados:

Exemplo
#grad {
  background-image: radial-gradient(red, yellow, green);
}
Gradiente radial - Paradas de cor com espaçamento diferente

O exemplo a seguir mostra um gradiente radial com paradas de cor espaçadas de forma diferente:

Exemplo
#grad {
  background-image: radial-gradient(red 5%, yellow 15%, green 60%);
}
Definir forma
O parâmetro de forma define a forma. Pode levar o valor círculo ou elipse. O valor padrão é elipse.

O exemplo a seguir mostra um gradiente radial com a forma de um círculo:

Exemplo
#grad {
  background-image: radial-gradient(circle, red, yellow, green);
}
ANÚNCIO

ANÚNCIO

Uso de palavras-chave de tamanhos diferentes
O parâmetro tamanho define o tamanho do gradiente. Pode assumir quatro valores:

lado mais próximo
lado mais distante
canto mais próximo
canto mais distante
Exemplo
Um gradiente radial com palavras-chave de tamanho diferente:

#grad1 {
  background-image: radial-gradient(closest-side at 60% 55%, red, yellow, black);
}

#grad2 {
  background-image: radial-gradient(farthest-side at 60% 55%, red, yellow, black);
}
Repetindo um gradiente radial
A função repeating-radial-gradient() é usada para repetir gradientes radiais:

Exemplo
Um gradiente radial repetitivo:

#grad {
  background-image: repeating-radial-gradient(red, yellow 10%, green 15%);
}


Exercicio

<estilo>
div {
  
______________:______________
(Branco Verde);
}
</estilo>

<corpo>
  <div style="height:200px"></div>
</body>


Gradientes Cônicos CSS
Um gradiente cônico é um gradiente com transições de cores giradas em torno de um ponto central.

Para criar um gradiente cônico, você deve definir pelo menos duas cores.

Sintaxe
background-image: conic-gradient([from angle] [at position,] color [degree], color [degree], ...);
Por padrão, o ângulo é 0deg e a posição é o centro.

Se nenhum grau for especificado, as cores serão distribuídas igualmente em torno do ponto central.

Gradiente Cônico: Três Cores
O exemplo a seguir mostra um gradiente cônico com três cores:

Exemplo
Um gradiente cônico com três cores:

#grad {
  background-image: conic-gradient(red, yellow, green);
}
Gradiente Cônico: Cinco Cores
O exemplo a seguir mostra um gradiente cônico com cinco cores:

Exemplo
Um gradiente cônico com cinco cores:

#grad {
  background-image: conic-gradient(red, yellow, green, blue, black);
}
Gradiente Cônico: Três Cores e Graus
O exemplo a seguir mostra um gradiente cônico com três cores e um grau para cada cor:

Exemplo
Um gradiente cônico com três cores e um grau para cada cor:

#grad {
  background-image: conic-gradient(red 45deg, yellow 90deg, green 210deg);
}
ANÚNCIO

Criar Gráficos de Pizza
Basta adicionar border-radius: 50%para fazer o gradiente cônico parecer uma torta:

Exemplo
#grad {
  background-image: conic-gradient(red, yellow, green, blue, black);
  border-radius: 50%;
}
Aqui está outro gráfico de pizza com graus definidos para todas as cores:

Exemplo
#grad {
  background-image: conic-gradient(red 0deg, red 90deg, yellow 90deg, yellow 180deg, green 180deg, green 270deg, blue 270deg);
  border-radius: 50%;
}
Gradiente cônico com ângulo de origem especificado
O [from angle ] especifica um ângulo pelo qual todo o gradiente cônico é girado.

O exemplo a seguir mostra um gradiente cônico com um ângulo de 90 graus:

Exemplo
Um gradiente cônico com um ângulo de origem:

#grad {
  background-image: conic-gradient(from 90deg, red, yellow, green);
}
Gradiente cônico com posição central especificada
A [ posição at ] especifica o centro do gradiente cônico.

O exemplo a seguir mostra um gradiente cônico com uma posição central de 60% 45%:

Exemplo
Um gradiente cônico com uma posição central especificada:

#grad {
  background-image: conic-gradient(at 60% 45%, red, yellow, green);
}
Repetindo um gradiente cônico
A repeating-conic-gradient()função é usada para repetir gradientes cônicos:

Exemplo
Um gradiente cônico repetitivo:

#grad {
  background-image: repeating-conic-gradient(red 10%, yellow 20%);
  border-radius: 50%;
}
Aqui está um gradiente cônico repetitivo com início e fim de cor definidos:

Exemplo
Um gradiente cônico repetitivo com início e fim de cor definidos:

#grad {
  background-image: repeating-conic-gradient(red 0deg 10deg, yellow 10deg 20deg, blue 20deg 30deg);
  border-radius: 50%;
}
Funções de Gradiente CSS
A tabela a seguir lista as funções de gradiente CSS:

Function	Description
conic-gradient()	Creates a conic gradient. Define at least two colors (around a center point)
linear-gradient()	Creates a linear gradient. Define at least two colors (top to bottom)
radial-gradient()	Creates a radial gradient. Define at least two colors (center to edges)
repeating-conic-gradient()	Repeats a conic gradient
repeating-linear-gradient()	Repeats a linear gradient
repeating-radial-gradient()	Repeats a radial gradient


Exemplo
Um gradiente cônico com três cores:

#grad {
  background-image: conic-gradient(red, yellow, green);
}

Mais exemplos de "Experimente você mesmo" abaixo.

Definição e Uso
A função conic-gradient() define um gradiente cônico como a imagem de fundo.

Um gradiente cônico é um gradiente com transições de cores giradas em torno de um ponto central.

Para criar um gradiente cônico, você deve definir pelo menos duas paradas de cor.

Exemplo de gradiente cônico:



Versão:	CSS3
Suporte do navegador
Os números na tabela especificam a primeira versão do navegador que suporta totalmente a função.

Function					
conic-gradient()	69.0	79.0	83.0	12.1	56.0
ANÚNCIO

ANÚNCIO

Sintaxe CSS
background-image: conic-gradient([from angle] [at position,] color degree, color degree, ...);
Value	Description
from angle	Optional. The entire conic gradient is rotated by this angle. Default value is 0deg
at position	Optional. Specifies the gradient center of the conic gradient. Default value is center
color degree, ..., color degree	Color stops are the colors you want to render smooth transitions among. This value consists of a color value, followed by an optional stop position (a degree between 0 and 360 or a percent between 0% and 100%).
Mais exemplos
Exemplo
Um gradiente cônico com cinco cores:

#grad {
  background-image: conic-gradient(red, yellow, green, blue, black);
}
Exemplo
Um gradiente cônico com três cores e um grau para cada cor:

#grad {
  background-image: conic-gradient(red 45deg, yellow 90deg, green 210deg)
}
Exemplo
Faça o gradiente cônico parecer uma torta adicionando border-radius: 50%:

#grad {
  background-image: conic-gradient(red, yellow, green, blue, black);
  border-radius: 50%;
}
Exemplo
Um gradiente cônico com um ângulo de origem:

#grad {
  background-image: conic-gradient(from 90deg, red, yellow, green);
  border-radius: 50%;
}
Exemplo
Um gradiente cônico com uma posição at:

#grad {
  background-image: conic-gradient(at 60% 45%, red, yellow, green);
  border-radius: 50%;
}
Exemplo
Um gradiente cônico com ângulo e posição:

#grad {
  background-image: conic-gradient(from 90deg at 60% 45%, red, yellow, green);
  border-radius: 50%;
}
Exemplo
Outro gráfico de pizza:

#grad {
  background-image: conic-gradient(red 0deg, red 90deg, yellow 90deg, yellow 180deg, green 180deg);
  border-radius: 50%;
}
Páginas Relacionadas
Tutorial de CSS: Gradientes de CSS

Função CSS linear-gradient()

Exemplo
Este gradiente linear começa no topo. Começa vermelho, passando para amarelo e depois para azul:

#grad {
  background-image: linear-gradient(red, yellow, blue);
}

Mais exemplos de "Experimente você mesmo" abaixo.

Definição e Uso
A função linear-gradient() define um gradiente linear como imagem de fundo.

Para criar um gradiente linear, você deve definir pelo menos duas paradas de cor. Interrupções de cores são as cores entre as quais você deseja renderizar transições suaves. Você também pode definir um ponto inicial e uma direção (ou um ângulo) junto com o efeito de gradiente.

Exemplo de Gradiente Linear:

Gradiente linear

Versão:	CSS3
Suporte do navegador
Os números na tabela especificam a primeira versão do navegador que suporta totalmente a função.

Números seguidos por -webkit-, -moz- ou -o- especificam a primeira versão que funcionou com um prefixo.

Function					
linear-gradient()	26.0
10.0 -webkit-	10.0	16.0
3.6 -moz-	6.1
5.1 -webkit-	12.1
11.1 -o-
ANÚNCIO

Sintaxe CSS
background-image: linear-gradient(direction, color-stop1, color-stop2, ...);
Value	Description
direction	Defines a starting point and a direction (or an angle) along with the gradient effect.
color-stop1, color-stop2,...	Color stops are the colors you want to render smooth transitions among. This value consists of a color value, followed by an optional stop position (a percentage between 0% and 100% or a length along the gradient axis).
Mais exemplos
Exemplo
Um gradiente linear que começa da esquerda. Começa vermelho, passando para azul:

#grad {
  background-image: linear-gradient(to right, red , blue);
}
Exemplo
Um gradiente linear que começa no canto superior esquerdo (e vai para o canto inferior direito):

#grad {
  background-image: linear-gradient(to bottom right, red , blue);
}
Exemplo
Um gradiente linear com um ângulo especificado:

#grad {
  background-image: linear-gradient(180deg, red, blue);
}
Exemplo
Um gradiente linear com várias paradas de cor:

#grad {
  background-image: linear-gradient(to right, red,orange,yellow,green,blue,indigo,violet);
}
Exemplo
Um gradiente linear com transparência:

#grad {
  background-image: linear-gradient(to right, rgba(255,0,0,0), rgba(255,0,0,1));
}


Função CSS radial-gradient()

Exemplo
Um gradiente radial com intervalos de cor uniformemente espaçados:

#grad {
  background-image: radial-gradient(red, green, blue);
}

Mais exemplos de "Experimente você mesmo" abaixo.

Definição e Uso
A função radial-gradient() define um gradiente radial como imagem de fundo.

Um gradiente radial é definido por seu centro.

Para criar um gradiente radial, você deve definir pelo menos duas paradas de cor.

Exemplo de gradiente radial:

Gradiente radial

Versão:	CSS3
Suporte do navegador
Os números na tabela especificam a primeira versão do navegador que suporta totalmente a função.

Números seguidos por -webkit-, -moz- ou -o- especificam a primeira versão que funcionou com um prefixo.

Function					
radial-gradient()	26.0
10.0 -webkit-	10.0	16.0
3.6 -moz-	6.1
5.1 -webkit-	12.1
11.6 -o-
ANÚNCIO

ANÚNCIO

Sintaxe CSS
background-image: radial-gradient(shape size at position, start-color, ..., last-color);
Value	Description
shape	Defines the shape of the gradient. Possible values:
ellipse (default)
circle
size	Defines the size of the gradient. Possible values:
farthest-corner (default)
closest-side
closest-corner
farthest-side
position	Defines the position of the gradient. Default is "center"
start-color, ..., last-color	Color stops are the colors you want to render smooth transitions among. This value consists of a color value, followed by an optional stop position (a percentage between 0% and 100% or a length along the gradient axis).
Mais exemplos
Exemplo
Um gradiente radial com cores espaçadas de forma diferente para:

#grad {
  background-image: radial-gradient(red 5%, green 15%, blue 60%);
}
Exemplo
Um gradiente radial com a forma de um círculo:

#grad {
  background-image: radial-gradient(circle, red, yellow, green);
}
Exemplo
Um gradiente radial com palavras-chave de tamanho diferente:

#grad1 {
  background-image: radial-gradient(closest-side at 60% 55%, blue, green, yellow, black);
}

#grad2 {
  background-image: radial-gradient(farthest-side at 60% 55%, blue, green, yellow, black);
}

Função CSS repeating-conic-gradient()

Exemplo
Um gradiente cônico repetitivo:

#grad {
  background-image: repeating-conic-gradient(red 10%, yellow 20%);
}
Mais exemplos de "Experimente você mesmo" abaixo.

Definição e Uso
A função repeating-conic-gradient() é usada para repetir gradientes cônicos.

Versão:	CSS3
Suporte do navegador
Os números na tabela especificam a primeira versão do navegador que suporta totalmente a função.

Function					
repeating-conic-gradient()	69.0	79.0	83.0	12.1	56.0
ANÚNCIO

ANÚNCIO

Sintaxe CSS
background-image: repeating-conic-gradient([from angle] [at position,] color degree, color degree, ...);
Value	Description
from angle	Optional. The entire conic gradient is rotated by this angle. Default value is 0deg
at position	Optional. Specifies the gradient center of the conic gradient. Default value is center
color degree, ..., color degree	Color stops are the colors you want to render smooth transitions among. This value consists of a color value, followed by an optional stop position (a degree between 0 and 360 or a percent between 0% and 100%).
Mais exemplos
Exemplo
Um gradiente cônico repetitivo com início e fim de cor definidos:

#grad {
  background-image: repeating-conic-gradient(red 0deg 30deg, yellow 30deg 60deg, blue 60deg 90deg);
}


Função CSS repeating-linear-gradient()

Exemplo
Um gradiente linear repetitivo:

#grad {
  background-image: repeating-linear-gradient(red, yellow 10%, green 20%);
}
Mais exemplos de "Experimente você mesmo" abaixo.

Definição e Uso
A função repeating-linear-gradient() é usada para repetir gradientes lineares.

Versão:	CSS3
Suporte do navegador
Os números na tabela especificam a primeira versão do navegador que suporta totalmente a função.

Números seguidos por -webkit-, -moz- ou -o- especificam a primeira versão que funcionou com um prefixo.

Function					
repeating-linear-gradient()	26.0
10.0 -webkit-	10.0	16.0
3.6 -moz-	6.1
5.1 -webkit-	12.1
11.1 -o-
ANÚNCIO

ANÚNCIO

Sintaxe CSS
background-image: repeating-linear-gradient(angle | to side-or-corner, color-stop1, color-stop2, ...);
Value	Description
angle	Defines an angle of direction for the gradient. From 0deg to 360deg. Default is 180deg.
side-or-corner	Defines the position of the starting-point of the gradient line. It consists of two keywords: the first one indicates the horizontal side, left or right, and the second one the vertical side, top or bottom. The order is not relevant and each of the keyword is optional.
color-stop1, color-stop2,...	Color stops are the colors you want to render smooth transitions among. This value consists of a color value, followed by an optional stop position (a percentage between 0% and 100% or a length along the gradient axis).
Mais exemplos
Exemplo
Diferentes gradientes lineares repetidos:

#grad1 {
  background-image: repeating-linear-gradient(45deg, red, blue 7%, green 10%);
}

#grad2 {
  background-image: repeating-linear-gradient(190deg, red, blue 7%, green 10%);
}

#grad3 {
  background-image: repeating-linear-gradient(90deg, red, blue 7%, green 10%);
}

Função CSS repeating-radial-gradient()

Exemplo
Um gradiente radial repetitivo:

#grad {
  background-image: repeating-radial-gradient(red, yellow 10%, green 15%);
}
Definição e Uso
A função repeating-radial-gradient() é usada para repetir gradientes radiais.

Versão:	CSS3
Suporte do navegador
Os números na tabela especificam a primeira versão do navegador que suporta totalmente a função.

Números seguidos por -webkit-, -moz- ou -o- especificam a primeira versão que funcionou com um prefixo.

Function					
repeating-radial-gradient()	26.0
10.0 -webkit-	10.0	16.0
3.6 -moz-	6.1
5.1 -webkit-	12.1
11.1 -o-


Sintaxe CSS
background-image: repeating-radial-gradient(shape size at position, start-color, ..., last-color);
Value	Description
shape	Defines the shape of the gradient. Possible values:
ellipse (default)
circle
size	Defines the size of the gradient. Possible values:
farthest-corner (default)
closest-side
closest-corner
farthest-side
position	Defines the position of the gradient. Default is "center"
start-color, ..., last-color	Color stops are the colors you want to render smooth transitions among. This value consists of a color value, followed by an optional stop position (a percentage between 0% and 100% or a length along the gradient axis).
