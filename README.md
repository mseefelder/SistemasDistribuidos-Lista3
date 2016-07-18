# SistemasDistribuidos-Lista3

1. 
	* Processo que chama e processo que executa função estão em máquinas diferentes, acarretando em espaços de endereçamento e ambiente computacional distintos;
	* Representação de dados diferentes (Little Endian, Big Endian);
	* Falhas de rede e das máquinas envolvidas.

### Extra: Little Endian vs. Big Endian

Sistemas representam vetores de bytes de maneiras diferentes. Considerando que temos uma *word* (32 *bits*) representada em hexadecimal por **0A0B0C0D**:

* Big Endian (**MSB primeiro**): Vai representar na memória (m[]) como m[0] = 0A; m[1] = 0B; m[2] = 0C; m[3] = 0D;
* Little Endian (**LSB primeiro**): Vai representar na memória (m[]) como m[0] = 0D; m[1] = 0C; m[2] = 0B; m[3] = 0A; 

2. 
	1. Cliente faz chamada de função para servidor de RPC e espera (bloqueante) mensagem de aceitação;
	2. Servidor de RPC recebe chamada de função e envia mensagem de aceitação para cliente. Servidor passa a executar procedimento local...;
	3. Cliente recebe aceitação, a chamada de função retorna mas ainda não há resultado. Cliente continua sua execução...;
	4. Ao terminar o procedimento, servidor envia resultado ao cliente via RPC;
	5. Mensagem de resultado gera uma interrupção no cliente, que por sua vez envia o reconhecimento de que recebeu a mensagem ao servidor.

### Extra: *Marshalling*, *Unmarshalling* e *Stubs*

Para evitar problemas por divergências nas representações de dados entre os participantes de um sistema de RPC, é feito o *marshalling* de mensagens a serem enviadas, convertendo a mensagem para uma representção de comum acordo entre os participantes. Ao receber uma mensagem, é feito o *unmarshalling* da mesma.

Tanto o *marshalling* quanto o *unmarshalling* são feitos pelos *stubs*, que são trechos de código fornecidos pelas biblioecas de RPC e tornam o envio e recebimento de chamadas e retornos de RPC transparentes aos usuários.

3. 

**Ordenação de eventos?**

4. 


5. 


6. 


7. 


8. 


9. 


10. 


11. 


12. 


13. 


14. 


15. 


16. 


17. 


18. 


19. 


20. 


21. 


22. 


23. 



## Revisar:

* aula 11
	* Falhas e Semântica em RPC;
	* RMI: vantagens e desvantagens
* 