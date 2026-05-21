📱 Troca de Telas – Navegação Entre Activities no Android
📌 Descrição do Projeto

O Troca de Telas é um aplicativo Android desenvolvido em Java no Android Studio com o objetivo de demonstrar como trabalhar com mais de uma tela (Activity) em uma aplicação.

O aplicativo possui:

🏠 Tela Principal (MainActivity) – exibe um botão para abrir a segunda tela.
📄 Segunda Tela (Tela2Activity) – exibe um botão para retornar à tela anterior.

A navegação entre as telas é realizada utilizando a classe Intent.

🎯 Objetivo

Praticar os conceitos fundamentais de:

Criação de múltiplas telas
Navegação com Intent
Uso do ConstraintLayout
Eventos de clique em botões
Encerramento de Activities com finish()
🛠️ Tecnologias Utilizadas
Java
Android Studio
XML
Android SDK
ConstraintLayout
📂 Estrutura do Projeto
app/

├── java/

│   └── br/ulbra/trocartela/

│       ├── MainActivity.java

│       └── Tela2Activity.java

│
├── res/

│   └── layout/

│       ├── activity_main.xml

│       └── activity_tela2.xml
│
└── AndroidManifest.xml

🖥️ Funcionalidades do Aplicativo
🏠 Tela Principal
Exibe o título Tela Principal
Possui o botão Ir para Tela 2
Abre a segunda tela com Intent
📄 Segunda Tela
Exibe o título Segunda Tela
Possui o botão Voltar
Retorna à tela principal usando finish()
🔄 Navegação Entre Telas
Abrindo a Segunda Tela
Intent intent = new Intent(
        MainActivity.this,
        Tela2Activity.class
);
startActivity(intent);
Retornando para a Tela Principal
finish();
📄 MainActivity.java

Responsável por iniciar a segunda tela ao clicar no botão.

Principais Componentes
Button btnTela2
Intent
startActivity()
📄 Tela2Activity.java

Responsável por fechar a Activity atual e retornar à tela anterior.

Principais Componentes
Button btnVoltar
finish()
📄 AndroidManifest.xml

O arquivo de manifesto registra as duas Activities do projeto.

<activity
    android:name=".Tela2Activity"
    android:exported="false" />

<activity
    android:name=".MainActivity"
    android:exported="true">
    <intent-filter>
        <action android:name="android.intent.action.MAIN" />
        <category android:name="android.intent.category.LAUNCHER" />
    </intent-filter>
</activity>
🧠 Conceitos Aplicados
Intent

Classe responsável por iniciar outra Activity.

startActivity()

Método que abre uma nova tela.

finish()

Encerra a Activity atual e retorna à tela anterior.

ConstraintLayout

Layout flexível utilizado para posicionar os componentes na tela.

▶️ Como Executar
Abra o projeto no Android Studio.
Execute em um emulador ou dispositivo Android.
Clique em Ir para Tela 2.
Na segunda tela, clique em Voltar.
✅ Resultado Esperado
A tela principal é exibida ao iniciar o app.
O botão abre corretamente a segunda tela.
O botão da segunda tela retorna para a tela principal.
📚 Conteúdos Praticados
Multiple Activities
Navegação entre telas
Eventos com botões
AndroidManifest
ConstraintLayout
👨‍💻 Autor

Projeto desenvolvido por Vitoria Gabriela Fernandes da Luz para fins acadêmicos na disciplina de Programação Mobile – ULBRA.
