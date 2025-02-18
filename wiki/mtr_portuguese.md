# [Debian] Debian Almquist Shell (dash) mtr uso: ferramenta de diagnóstico de rede

## Overview
O comando `mtr` (My Traceroute) combina as funcionalidades de `traceroute` e `ping`, permitindo que os usuários analisem a rota que os pacotes de dados percorrem até um host específico e verifiquem a qualidade da conexão em cada salto.

## Usage
A sintaxe básica do comando `mtr` é a seguinte:

```bash
mtr [opções] [host]
```

## Common Options
Aqui estão algumas opções comuns do `mtr`:

- `-r`: Executa o `mtr` em modo relatório, exibindo os resultados de forma mais compacta.
- `-c <n>`: Define o número de pacotes a serem enviados (substitua `<n>` pelo número desejado).
- `-i <n>`: Define o intervalo entre os pacotes enviados (substitua `<n>` pelo valor em segundos).
- `-p`: Executa o `mtr` em modo de exibição de portas, mostrando as portas usadas para a conexão.

## Common Examples
Aqui estão alguns exemplos práticos do uso do `mtr`:

1. **Executar um mtr simples para um host:**
   ```bash
   mtr google.com
   ```

2. **Executar mtr em modo relatório:**
   ```bash
   mtr -r google.com
   ```

3. **Enviar um número específico de pacotes:**
   ```bash
   mtr -c 10 google.com
   ```

4. **Definir um intervalo entre pacotes:**
   ```bash
   mtr -i 1 google.com
   ```

5. **Executar mtr mostrando as portas:**
   ```bash
   mtr -p google.com
   ```

## Tips
- Utilize o modo relatório (`-r`) para obter uma visão geral rápida da qualidade da conexão.
- Experimente diferentes valores para o número de pacotes (`-c`) e o intervalo (`-i`) para ajustar o teste às suas necessidades.
- Combine o `mtr` com outras ferramentas de rede para diagnósticos mais completos, como `ping` e `traceroute`.