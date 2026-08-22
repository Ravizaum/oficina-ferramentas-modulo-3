# Alterações no código

**Arquivo:** `plugins/frete.py`

- Classe `FreteCorrespondenciaPlugin`: constante `ISENCAO_ACIMA_DE` elevada
  de `5_000.00` para `50_000.00`.

```diff
-    ISENCAO_ACIMA_DE = 5_000.00   # frete grátis para faturas acima desse valor
+    ISENCAO_ACIMA_DE = 50_000.00   # frete grátis para faturas acima desse valor
```