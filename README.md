# alphamask-modelos

Espelho dos modelos ONNX de código aberto que o [Alpha Mask](https://alphamask.com.br/)
baixa na primeira execução.

Este repositório existe por **disponibilidade**, não por propriedade. Os dois
arquivos abaixo são de terceiros, já públicos, e foram apenas copiados sem
nenhuma alteração — os SHA-256 são os mesmos dos originais. O Alpha Mask
dependia de um release de outro projeto continuar no ar; se aquele endereço
mudasse, nenhuma instalação nova conseguiria baixar o modelo. Um espelho próprio
resolve isso.

**Aqui não há nada do Alpha Mask além desta página.** Sem código, sem o
pipeline de pré e pós-processamento, sem chave, sem dado de cliente.

## Arquivos

| Arquivo | Tamanho | SHA-256 | Origem | Licença |
|---|---|---|---|---|
| `u2net.onnx` | 175.997.641 B | `8d10d2f3bb75ae3b6d527c77944fc5e7dcd94b29809d47a739a7a728a912b491` | [U²-Net](https://github.com/xuebinqin/U-2-Net), distribuído pelo [rembg](https://github.com/danielgatis/rembg) | Apache-2.0 |
| `BiRefNet-general-bb_swin_v1_tiny-epoch_232.onnx` | 224.005.088 B | `5600024376f572a557870a5eb0afb1e5961636bef4e1e22132025467d0f03333` | [BiRefNet](https://github.com/ZhengPeng7/BiRefNet) por ZhengPeng7, distribuído pelo rembg | MIT |

Os dois estão nos *assets* do release, não no histórico do git.

## Verificar antes de usar

```
shasum -a 256 u2net.onnx
```

O hash tem que bater com a tabela acima. O Alpha Mask faz essa conferência
sozinho a cada download e recusa o arquivo se não bater.

## Licenças

Os textos originais estão em [`licencas/`](licencas/):

- `U-2-Net-Apache-2.0.txt` — Apache License 2.0, do repositório U²-Net.
- `BiRefNet-MIT.txt` — MIT, © 2024 ZhengPeng.
- `rembg-MIT.txt` — MIT, © 2020 Daniel Gatis, do projeto que empacota e
  distribui os dois arquivos em formato ONNX.

Nenhum direito sobre os modelos é reivindicado aqui. Crédito e autoria são dos
respectivos autores.
