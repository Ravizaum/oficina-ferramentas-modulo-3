# Alterações no código

**Arquivo:** `main.py`

- Definição da `Vaga`: campo `salario_maximo` reduzido de `18_000.0` para
  `12_000.0`.

```diff
     vaga = Vaga(
         id=1,
         titulo="Engenheiro(a) de Software Backend",
         experiencia_minima=3,
         habilidades_requeridas=["Python", "PostgreSQL", "Docker", "REST"],
-        salario_maximo=18_000.0,
+        salario_maximo=12_000.0,
     )
```