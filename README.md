# api_zabbix_bi
# Exemplo de como conectar o Zabbix com o Power Bi direto via API sem utilização de scripts externos.

# No campo de "Transformar dados" crie uma consulta com valor texto para seu ZabbixAPI e para o ZabbixToken
# Crie outra consulta com "Obter Dados/Consulta Nula"
# Abra o "Editor Avançado" da consulta e adicione o Script "ZabbixUser" e modifique conforme sua necessidade.

# Para realizar a consulta é necessário passar o Token de usuário, o qual pode ser obtido diretamente do front-end do Zabbix e a URL na API do seu servidor Zabbix. 
![Captura de tela 01](https://github.com/samuelsrn/api_zabbix_bi/assets/63984940/b8effc3f-38d4-40b1-9138-8aeeca599edb)
![Captura de tela 02](https://github.com/samuelsrn/api_zabbix_bi/assets/63984940/af876799-4b7f-49aa-918b-f192c52a3073)

# altere o Bady no Script da consulta para obter diferentes métricas.
Body =
    "{
        ""jsonrpc"": ""2.0"",
        ""method"": ""host.get"",
        ""params"": {
            ""groupids"": [95]
        },
        ""auth"": """ & token & """,
        ""id"": 1
    }",

# No exemplo estou utilizando o groupID do meu zabbix server.
  
