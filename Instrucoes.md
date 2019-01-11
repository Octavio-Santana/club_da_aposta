# Instruções para utilizar o conjunto de dados para o processo Seletivo: Cientista de Dados Júnior do Clube da Aposta

Muito obrigado pelo seu interesse em participar do nosso processo seletivo! =) Lembre-se que para obter mais informações sobre essa vaga você pode acessar o https://www.clubedaposta.com/carreiras.

Fizemos o possível para tornar a sua tarefa o mais simples que pudemos. Dentro dessa pasta vocô terá o conjunto de dados 'base-dados-clube-da-aposta.json', esse é um arquivo no formato json, que pode ser aberto facilmente através da biblioteca Pandas.

## Sugestão de ordens para as colunas

Ao carregar o conjunto de dados pela primeira vez, as colunas serão ordenadas em ordem alfabética, mas para facilitar a sua compreensão desse conjunto, sugerimos que você as ordene da seguinte forma:

ordens_coluna = ['home_name', 'away_name', 'home_score', 'away_score', 'final_result',
       'time', 'home_pos', 'away_pos', 'round', 'home_last5all_home',
       'home_last5all_home_win', 'home_last5all_home_draw',
       'home_last5all_home_lose', 'away_last5all_away',
       'away_last5all_away_win', 'away_last5all_away_draw',
       'away_last5all_away_lose', 'last5all_home_away_dif', 'fifa_home_ova',
       'fifa_home_att', 'fifa_home_mid', 'fifa_home_def', 'fifa_away_ova',
       'fifa_away_att', 'fifa_away_mid', 'fifa_away_def', 'elo_home_score',
       'elo_away_score', 'tfm_value_home', 'tfm_value_away']

Assim, digamos que você carregue o arquivo json em um dataframe 'df', basta digitar:

df = df[ordens_coluna]

Vamos entender o que significa cada uma das variáveis:

## Entendendo as variáveis

1. 'home_name': Nome do mandante,
2. 'away_name': Nome do visitante,
3. 'home_score': Gols feitos pelo mandante na partida
4. 'away_score': Gols feitos pelo visitante na partida, 
5. 'final_result': Essa é a variável que queremos prever, trata-se do resultado final, sendo H (Home) Vitória do Mandante, D (Draw) Empate, e, por fim, A (Away) visitante,
6. 'time': Tempo em formato unix, 
7. 'home_pos': A posição do mandante antes dessa partida, 
8. 'away_pos': A posição do visitante antes dessa partida, 
9. 'round': A rodada do campeonato, 
10. 'home_last5all_home': Saldo de gols do mandante nas últimas 5 partidas,
11. 'home_last5all_home_win': Nº de vitórias do mandante nas últimas 5 partidas,
12. 'home_last5all_home_draw': Nº de empates do mandante nas últimas 5 partidas,
13. 'home_last5all_home_lose': Nº de derrotas do mandante nas últimas 5 partidas,
14. 'away_last5all_away': Saldo de gols do visitante nas últimas 5 partidas,
15. 'away_last5all_away_win': Nº de vitórias do visitante nas últimas 5 partidas,
16. 'away_last5all_away_draw': Nº de empates do visitante nas últimas 5 partidas,
17. 'away_last5all_away_lose': Nº de derrotas do visitante nas últimas 5 partidas,
18. 'last5all_home_away_dif': A diferença do saldo entre as equipes, ou seja: 'home_last5all_home' - 'away_last5all_away'
19. 'fifa_home_ova': Score Geral do Mandante no Fifa
20. 'fifa_home_att': Score de ataque do Mandante no Fifa
21. 'fifa_home_mid': Score de meio de campo do Mandante no Fifa
22. 'fifa_home_def': Score de defesa do Mandante no Fifa
23. 'fifa_away_ova': Score Geral do Visitante no Fifa
24. 'fifa_away_att': Score de ataque do Visitante no Fifa
25. 'fifa_away_mid': Score de meio de campo do Visitante no Fifa
26. 'fifa_away_def': Score de defesa do Visitante no Fifa  
27. 'elo_home_score': Score Elo do Mandante
28. 'elo_away_score': Score Elo do Visitante 
29. 'tfm_value_home': Valor de mercado do elenco mandante em Euros
30. 'tfm_value_away': Valor de mercado do elenco visitante em Euros

Estamos aqui com um problema de aprendizagem supervisionada, uma classificação. A variável dependente (target value) é o 'final_result', que possui 3 possíveis valores: H, D ou A, assim ela será o 'y' da sua modelagem. Ao criar a matriz de variáveis não esqueça de remover 'home_score' e 'away_score', afinal se o algoritmo sabe o placar final da partida ele será capaz de fazer previsões 100% acuradas. =)


## Lembrete final

Dé preferência em utilizar o Jupyter Notebook, ao terminar de criar o seu código, você precisará gravar a sua tela e nos explicar com a sua voz etapa por etapa, compartilhando um pouco do seu raciocínio e das suas escolhas. Analise as saídas e diga-nos um pouco sobre a métrica que você escolheu.

Feito isso, suba esse vídeo para o Youtube, Google Drive ou o serviço que você preferir e, depois, basta acessar o formulário de participação para essa vaga, que está em www.clubedaposta.com/carreiras, e acessar o formulário para a vaga que está por lá. Preencha com seus dados pessoais, seu currículo, e insera um link que possamos acessar o seu vídeo e a cópia do seu código.

Verifique se os links estão acessíveis para a gente! Afinal, as vezes esquecemos de mudar as configurações de privacidade.

Fique tranquilo que nessa etapa não queremos nada muito sofisticado, apenas saber se você tem os fundamentos de Machine Learning que precisamos aqui no Clube da Aposta. ;)

Boa sorte e estamos na torcida por você! \o/