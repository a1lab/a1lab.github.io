# Visibilidade e modificadores de acesso

* servem para definir que partes da classe estão acessíveis para outras classes do sistema
* só é possível usar um modificador por vez

* Toda classe ou interface devem ser públicas, exceto se forem aninhadas
* O mesmo se aplica às enumerações, que são tipos especiais de classes
* membros (construtores, métodos e atributos) podem ser publicos, privados, protegidos ou padrão
* variáveis locais e parâmetros não podem receber modificadores de acesso

* classes, enums e interfaces aninhadas podem receber qualquer modificador de visibilidade, pois são consideradas membros

## public

* um atributo ou método public pode ser acessado de qualquer lugar do sistema

## protected

* membros delcarados com o modificador _protected_ podem ser acessados somente por subtipos da classe na qual foram declarados ou por outros tipos contidos no mesmo pacote
* uma classe pode estender outra mesmo estando em pacotes diferentes

## default

* se nenhum modificador de acesso for definido, a visibilidade é default, ou seja, só é visível dentro do pacote
* a visibilidade default também é chamada de package private, isso pq ela é mais restritiva que a visibilidade protected
* se uma classe A tem um método default e uma classe B herda de A, sendo que B está em outro pacote, então B não poderá acessar o método default
* se o método fosse protected, poderia
* a palvbra chave defautl é usada em um switch ou em anotações. Para usar a visibilidade default, basta omitir a visibilidade
* default também pode ser usado para definir a implementacao inicial de um metodo

* se declararmos uma classe default, mesmo que seus membros tenham visibilidade diferente, ela só poderá ser instanciada dentro do mesmo pacote, portanto todos os modificadores terão a visibilidade reduzida

# private

* membros definidos como private são acessíveis somente dentro da propria classe
* nem mesmo seus subtipos podem acessá-los
* classes aninhadas podem acessar membros privados
* métodos privados e default não podem ser sobrescritos

