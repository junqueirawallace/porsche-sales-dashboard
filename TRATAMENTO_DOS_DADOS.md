# Nota de tratamento dos dados

A dashboard incorpora somente campos sanitizados necessários à análise. Foram omitidos nomes de clientes e vendedores e todas as versões cruas dos campos. Os 100 registros foram preservados. A coluna de data sanitizada não é utilizada nos cálculos porque parte dos valores está marcada como `INVALID`; assim evitamos inferir datas. O preço sanitizado é tratado como número e a soma é calculada a partir desses valores. Os filtros utilizam modelo, estado, ano do veículo e método de pagamento.
