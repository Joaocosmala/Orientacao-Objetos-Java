# Estrutura Básica de um Código Java (com Interface Gráfica - Swing)

## Fase 1 — Declarar os componentes da interface gráfica
Declare todos os componentes como atributos da classe.

import javax.swing.*;

public class MinhaTela {
    private JFrame frame;
    private JButton botao;
    private JLabel label;
}

---

## Fase 2 — Construir os componentes da interface gráfica
Instanciar e configurar os componentes no construtor.

public MinhaTela() {
    frame = new JFrame("Minha Aplicação");
    botao = new JButton("Clique aqui");
    label = new JLabel("Texto inicial");

    frame.setSize(400, 300);
    frame.setDefaultCloseOperation(JFrame.EXIT_ON_CLOSE);
    frame.setLayout(null);

    botao.setBounds(120, 100, 150, 30);
    label.setBounds(150, 50, 150, 30);
}

---

## Fase 3 — Adicionar os componentes ao JFrame
Adicionar os componentes ao frame e torná-lo visível.

public void iniciar() {
    frame.add(botao);
    frame.add(label);

    frame.setVisible(true);
}

---

## Fase 4 — Execução
Criar o método main para iniciar a aplicação.

public static void main(String[] args) {
    MinhaTela tela = new MinhaTela();

    tela.iniciar();
}
