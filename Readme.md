# Anotações

- 603 codigo de declined
- 486 Busy
- ver web assembly, webGL/CL
  - edge computing

objeto tipo lista com interação sempre deve estar atualizada na borda

```javascript
 this.game.socket.on("jogadores", (jogadores) => {
      if (jogadores.primeiro === this.game.socket.id) {
        navigator.mediaDevices
          .getUserMedia({ video: false, audio: true })
          .then((stream) => {
            this.game.midias = stream;
          })
          .catch((error) => console.log(error));

```

objeto -> botão para discar, botões com eventos
- comunicação assincrona
- - eventos
  -push notification/pubSub

```javascript
 this.salas.forEach((item) => {
      item.botao = this.add
        .text(item.x, item.y, "[Sala " + item.numero + "]", {
          fontFamily: "monospace",
          font: "32px Courier",
          fill: "#cccccc",
        })
        .setInteractive(); //interação
                          //registro de evento -> usuário 
                                             //-> rede
      item.botao.on("pointerdown", () => {
        this.mensagem.setText("Aguardando segundo jogador...");
        
        this.salas.forEach((item) => {
          item.botao.destroy();
        });
        
        this.sala = item.numero;
        
        console.log("Pedido de entrada na sala %s.", this.sala);

        if (this.game.registro) {
          this.game.socket.emit("entrar-na-sala", this.sala);
        } else {
          console.log("Usuário não registrado no servidor.")
        }
      });
    });
```


para as listas usar set()

```javascript

```

```javascript

```




https://engineering.fb.com/
  banana bread
  https://playcanvas.com/explore


