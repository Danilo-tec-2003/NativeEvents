                                                                                  ANOTAÇÕES SOBRE MEU ESTUDO REFERENTE A EVENTOS E FUNÇÕES (REACT NATIVE)
                                                                                  
Função Inline:
Utilize funções inline para ações simples que não requerem reutilização ou lógica complexa. Essas funções são definidas diretamente dentro do componente.
Exemplo: 
<Text onPress={() => console.log("Inline function triggered")}>Inline</Text>

Função Handler: 
Defina funções separadas para manter o código organizado e reutilizável. Ideal para funções que não precisam de parâmetros.
Exemplo:
// Função handler definida separadamente
async function handlerHelloWorld() {
  console.log("Hello from handler function");
}
// Uso no componente
<Text onPress={handlerHelloWorld}>Handler Function</Text>

Função com Parâmetros
Quando precisar passar dados para a função, como ao interagir com uma API, utilize funções que aceitam parâmetros.
Exemplo:
// Função que aceita um parâmetro
function handlePress(param) {
  console.log(`Parameter received: ${param}`);
}
// Uso no componente
<Text onPress={() => handlePress(1)}>Function with Parameters</Text>

Função de Outro Arquivo
Para funções que você deseja compartilhar entre diferentes componentes, exporte e importe-as conforme necessário.
Exemplo:
// Exportando a função de outro arquivo
export function helloDarthVader() {
  console.log("Hello from another file");
}
// Importando e utilizando no componente
<Text onPress={helloDarthVader}>Function from Another File</Text>


- Principais Eventos

.onPress
Disparado quando o usuário toca e solta o dedo no componente. Ideal para ações que devem ocorrer após o toque ser completado.
Exemplo:
<Text onPress={() => console.log("Press event triggered")}>Press</Text>

.onPressIn
Disparado assim que o dedo toca o componente, útil para ações imediatas como iniciar uma animação ou alterar o estado visual do botão.
Exemplo:
<Text onPressIn={() => console.log("Press In event triggered")}>Press In</Text>

.onPressOut
Disparado quando o usuário levanta o dedo do componente, mesmo que o toque tenha sido iniciado fora do componente. Útil para detectar interrupções de toque e fornecer feedback visual.
Exemplo:
<Text onPressOut={() => console.log("Press Out event triggered")}>Press Out</Text>

.onLongPress
Disparado quando o usuário realiza um toque longo (segura o dedo no componente). Ideal para ações que requerem um toque prolongado.
Exemplo:
<Text onLongPress={() => console.log("Long Press event triggered")}>Long Press</Text>

.onTextLayout
Disparado quando o texto é renderizado no layout, útil para ações relacionadas ao layout ou ao carregamento de texto.
Exemplo:
<Text onTextLayout={() => console.log("Text Layout event triggered")}>Text Layout</Text>
