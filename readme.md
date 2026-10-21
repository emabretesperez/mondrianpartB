# Perte B Mondrian

## Parte 2 - Movimento com random

Duas das linhas pretas tremem: uma vertical e uma horizontal.

**Como funciona**

- `setup()` corre uma vez e cria o canvas.
- `draw()` corre sempre,  e redesenha o quadro todo.
- `random(-4, 4)` devolve um número aleatório entre -4 e 4, diferente em cada imagem.
- Esse número é somado à posição da linha, por isso a linha muda um pouco de sítio a cada imagem e parece que treme.

**Tremor, usado para mexer a linha**

`let tremor1 = random(-4, 4);`
`let tremor2 = random(-4, 4);`

- linha vertical: o tremor soma-se ao x
line(width/2-33 + tremor1, 0, width/2-33 + tremor1, height);

- linha horizontal: o tremor soma-se ao y
line(0, height/2-71.98 + tremor2, width, height/2-71.98 + tremor2);
```

**Como se soma o tremor**

- Na linha vertical, muda-se o x e a linha anda da direta para a esquerda e vice versa
- Na linha horizontal, muda-se o y e a linha anda de cima para baixo.