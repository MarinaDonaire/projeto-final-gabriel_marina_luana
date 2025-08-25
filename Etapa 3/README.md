Para testar a aplicação ver : https://github.com/EmbarcaTech-2025/projeto-final-gabriel_marina_luana/tree/main/monitor_energia

**Não se esqueça de alterar as credenciais para os seus dados de rede e API KEY**

**Visão Geral do Projeto**

O projeto consiste em um sistema embarcado para monitorar a tensão e corrente elétrica em tempo real de um sistema, sejá de um eletrodoméstico isolado, ou da rede total da residência, utilizando uma Raspberry Pi Pico W. A ideia é fornecer um método simples e acessível para monitoramento residencial e até industrial para previnir danos a equipamentos e garantir que a cobrança de concessionárias de energia elétricas estão contabilizando de maneira correta o consumo e repassando o valor correto ao cliente. O sistema é capaz de fazer o monitoramento e enviar os dados em tempo real via Wifi para a plataforma ThingSpeak. 

**Funcionalidades do Sistema**

• Driver do Cartão SD: Foi desenvolvido um driver de software modular, capaz de inicializar a comunicação via SPI com o cartão SD e gerenciar a escrita de arquivos. A pinagem utilizada é: MISO no GP16, CS no GP17, SCK no GP18 e MOSI no GP19.

• Registro de Dados: O sistema agora pode criar um arquivo CSV com cabeçalhos (timestamp, tensão_rms, corrente_rms, energia_consumida, status_tensao), e adicionar novas linhas de dados a cada ciclo de execução.

• Timestamp: O código utiliza o Relógio de Tempo Real (RTC) da Pico para marcar o horário exato de cada medição, permitindo um registro preciso e sequencial dos dados.

• Leitura dos  Sensores: O código faz as leituras de tensão e corrente, mandando os dados em tempo real para o ThingSpeak e registra esses dados no cartão SD. Sendo possível compilar e simular as leituras de tensão e corrente, permitindo que a funcionalidade de gravação e conexão Wifi seja verificada sem a necessidade dos sensores físicos ZMPT101B e SCT-013, sendo também possível compilar usando a opção hw real, usando os sensores fisícos. 

**Implementações para as próximas etapas**

• Adicionar a funcionalidade de visualização física pelo display OLED SSD1306 presente na placa BitDogLab, visando um feedback visual na área da medição, não dependendo de conexão Wifi para caso haja falha. 


Link demonstrando o funcionamento : https://www.youtube.com/watch?v=ijfBzkFrV8M

Imagem do Hardware : <img width="960" height="1280" alt="image" src="https://github.com/user-attachments/assets/6256e77b-1d6c-4a1f-8687-3044d4063547" />
