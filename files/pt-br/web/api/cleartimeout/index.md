---
title: WindowTimers.clearTimeout()
slug: Web/API/clearTimeout
tags:
  - API
  - Method
  - Window
translation_of: Web/API/WindowOrWorkerGlobalScope/clearTimeout
original_slug: Web/API/WindowOrWorkerGlobalScope/clearTimeout
---
{{APIRef("HTML DOM")}}

## Sumário

O método **`clearTimeout()`** do escopo\_ _{{domxref("WindowOrWorkerGlobalScope")}} cancela um \_timeout_ previamente estabelecido pela função {{domxref("WindowOrWorkerGlobalScope.setTimeout", "setTimeout()")}}.

## Síntaxe

```
escopo.clearTimeout(timeoutID)
```

### Parâmetros

- `timeoutID`
  - : O ID do _timeout_ que você deseja cancelar. Esse ID é o retorno da função `setTimeout()`.

É interessante ressaltar que os conjuntso de \_ID_s usados pelos métodos {{domxref("WindowOrWorkerGlobalScope.setTimeout", "setTimeout()")}} e {{domxref("WindowOrWorkerGlobalScope.setInterval", "setInterval()")}} são compartilhados, o que significa que `clearTimeout()` e {{domxref("WindowOrWorkerGlobalScope.clearInterval", "clearInterval()")}} podem ser tecnicamente utilizados de forma intercambiável. No entanto, para obter-se maior clareza, isso deve ser evitado.

## Exemplo

Execute o script abaixo em uma página web e clique na página uma vez. Você verá uma mensagem aparecer um segundo depois. Se você continuar clicando na página várias vezes nesse intervalo de tempo, a mensagem aparecerá uma única vez.

```js
var alarme = {
  relembrar: function(aMessage) {
    alert(aMessage);
    delete this.timeoutID;
  },

  setup: function() {
    if (typeof this.timeoutID === 'number') {
        this.cancelar();
    }

    this.timeoutID = window.setTimeout(function(msg) {
        this.relembrar(msg);
    }.bind(this), 1000, 'Wake up!');
  },

  cancelar: function() {
    window.clearTimeout(this.timeoutID);
  }
};
window.onclick = function() { alarme.setup() };
```

## Notas

Passar um _ID_ inválido para `clearTimeout` não causa nenhum efeito (não lança nenhuma exceção).

## Especificações

| Especificação                                                                                                                                    | Status                           | Comentário                                       |
| ------------------------------------------------------------------------------------------------------------------------------------------------ | -------------------------------- | ------------------------------------------------ |
| {{SpecName('HTML WHATWG', 'webappapis.html#dom-cleartimeout', 'WindowOrWorkerGlobalScope.clearTimeout()')}} | {{Spec2("HTML WHATWG")}} | Método movido para `WindowOrWorkerGlobalScope` . |
| {{SpecName('HTML WHATWG', 'webappapis.html#dom-cleartimeout', 'clearTimeout()')}}                                     | {{Spec2('HTML WHATWG')}} |                                                  |

## Compatibilidade

{{Compat("api.WindowOrWorkerGlobalScope.clearTimeout")}}

## Veja também

- {{domxref("WindowOrWorkerGlobalScope.setTimeout()")}}
- {{domxref("WindowOrWorkerGlobalScope.setInterval()")}}
- {{domxref("WindowOrWorkerGlobalScope.clearInterval()")}}
- {{domxref("Window.requestAnimationFrame()")}}
- [_Daemons_ management](/pt-BR/docs/JavaScript/Timers/Daemons)