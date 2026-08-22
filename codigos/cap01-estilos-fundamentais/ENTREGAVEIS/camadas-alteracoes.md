# Alterações no código

**Arquivo:** `dominio.py`

- Import: adicionado `timedelta` (`from datetime import datetime, timedelta`).
- Classe `Horario`: adicionada constante `BUFFER_MINUTOS = 60` e o método
  `conflita_com` passou a exigir esse intervalo mínimo entre horários,
  em vez de checar apenas sobreposição direta.

```diff
-    def conflita_com(self, outro: Horario) -> bool:
-        """Retorna True se os dois horários se sobrepõem."""
-        return self.inicio < outro.fim and self.fim > outro.inicio
+    BUFFER_MINUTOS = 60
+
+    def conflita_com(self, outro: Horario) -> bool:
+        buffer = timedelta(minutes=self.BUFFER_MINUTOS)
+        return self.inicio < (outro.fim + buffer) and (self.fim + buffer) > outro.inicio
```