# altran-desafio
Qual inteiro positivo abaixo de 1 milhão produz a sequencia com mais items? 

            function seqMontagem(numNatural) {
                var contagem = 1;
                while (numNatural != 1) {
                    if ((numNatural%2) == 0) 
                    {
                        numNatural = numNatural/2;
                    }
                    else 
                    {
                        numNatural = (numNatural*3)+1;
                    }
                    contagem++;
                }
                return contagem;
            }
        
            var numMax;
            var seqMax = 0;
        
            for (var contagem = 1; contagem < 1000000; contagem++) 
            {
                var seq = seqMontagem(contagem);
                if (seq > seqMax) 
                {
                    numMax = contagem;
                    seqMax = seq;            
                }
            }   
