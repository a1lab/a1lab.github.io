
# Tipos primitivos

Em Java, as variáveis são estaticamente tipadas, ou fortemente tipadas, o que significa que elas devem ser declaradas antes de serem utilizadas.
A declaração de uma variável é uma sentença em que são definidos seu nome e tipo de dado. 
O tipo de dado determina os valores que a variável pode conter e as operações que podem ser feitas sobre elas.
Os tipos de dados dividem-se em dois conjuntos: os tipos primitivos, que são definidos pela própria linguagem de programação; e os tipos de referência, que são definidos pelo programador.
Os tipos primitivos java são 7: *boolean, byte, short, int, long, float, double* e *char*. 

<html>
	<table>
		<tr>
			<th>Nome</th>
			<th>Tipo</th>
			<th>Tamanho</th>
			<th>Faixa de valores</th>
			<th>Valor <i>default</i></th>
		</tr>
		<tr>
			<td>boolean</td>
			<td>inteiro</td>
			<td>1 bit</td>
			<td>{true, false}</td>
			<td>false</td>
		</tr>
		<tr>
			<td>byte</td>
			<td>inteiro</td>
			<td>8 bits</td>
			<td>[-2^8 , 2^8 -1]</td>
			<td>0</td>
		</tr> 
		<tr>
			<td>short</td>
			<td>inteiro</td>
			<td>16 bits</td>
			<td>[-2^16, 2^16 -1]</td>
			<td>0</td>
		</tr> 
		<tr>
			<td>int</td>
			<td>inteiro</td>
			<td>32 bits</td>
			<td>[-2^32 , 2^32-1]</td>
			<td>0</td>
		</tr> 
		<tr>
			<td>long</td>
			<td>inteiro</td>
			<td>64bits</td>
			<td>[2^64 , 2^64 -1]</td>
			<td>0L</td>
		</tr> 
		<tr>
			<td>float</td>
			<td>decimal</td>
			<td>32bits</td>
			<td>precisão simples</td>
			<td>0.0F</td>
		</tr> 
		<tr>
			<td>double</td>
			<td>decimal</td>
			<td>64bits</td>
			<td>precisão dupla</td>
			<td>0.0</td>
		</tr> 
		<tr>
			<td>char</td>
			<td>inteiro</td>
			<td>[0 , 1114111]</td>
			<td>Unicode</td>
			<td>'u0000' (ou 0)</td>
		</tr>  
	</table>
</html>

* Nem *float*, nem *double* (apesar da precisão dupla) devem ser utilizados para representar valores monetários. Ao invés disso, sugere-se o uso da classe BigDecimal.

* Ao contrário dos campos de uma classe, os parâmetros de um método não possuem valores _default_. 
* Todas as variáveis locais devem ser inicializadas antes de serem utilizadas, caso contrário o programa causará um erro de compilação.
