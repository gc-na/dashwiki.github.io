# [Português] Debian Almquist Shell (dash) hostname uso: exibir ou definir o nome do host

## Overview
O comando `hostname` é utilizado para exibir ou definir o nome do host do sistema. O nome do host é um identificador que permite que o sistema seja reconhecido em uma rede. Esse comando é fundamental para a configuração de redes e para a identificação de máquinas em um ambiente.

## Usage
A sintaxe básica do comando `hostname` é a seguinte:

```bash
hostname [opções] [argumentos]
```

## Common Options
Aqui estão algumas opções comuns do comando `hostname`:

- `-f`, `--fqdn`: Exibe o nome de domínio totalmente qualificado (FQDN) do host.
- `-i`, `--ip-address`: Exibe o endereço IP do host.
- `-s`, `--short`: Exibe apenas o nome curto do host.
- `-d`, `--domain`: Exibe o nome do domínio do host.

## Common Examples
Aqui estão alguns exemplos práticos do uso do comando `hostname`:

1. Exibir o nome do host atual:
   ```bash
   hostname
   ```

2. Exibir o nome de domínio totalmente qualificado:
   ```bash
   hostname -f
   ```

3. Exibir o endereço IP do host:
   ```bash
   hostname -i
   ```

4. Exibir apenas o nome curto do host:
   ```bash
   hostname -s
   ```

5. Definir um novo nome de host:
   ```bash
   sudo hostname novo-nome
   ```

## Tips
- Sempre utilize `sudo` ao definir um novo nome de host, pois é necessário ter permissões de administrador.
- Após alterar o nome do host, pode ser necessário reiniciar o sistema ou o serviço de rede para que as alterações tenham efeito.
- Para garantir que o novo nome de host persista após reinicializações, edite o arquivo `/etc/hostname`.