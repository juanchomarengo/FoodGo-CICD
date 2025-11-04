# Guía Demo CI/CD - FoodGo

## Flujo de la Demo (5 minutos)

### ANTES DE PRESENTAR:
- ✅ Crea un Work Item en Azure Boards (anota el ID, ejemplo: #22)
- ✅ Abre 2 pestañas: GitHub y Azure DevOps Boards

---

### PASO 1: Mostrar estado inicial (30seg)
1. Muestra **Azure Boards** → Ticket en "To Do"
2. Muestra **GitHub** → Pestaña "Actions"
3. Di: *"Voy a implementar esta feature y verán cómo se automatiza todo"*

---

### PASO 2: Hacer cambios (1min)

Reemplaza `22` con el ID de tu Work Item:

```bash
git checkout -b feature/AB#22-nueva-feature
echo "- Feature implementada" >> README.md
git add README.md
git commit -m "Implementar nueva feature. Fixes AB#22"
git push origin feature/AB#22-nueva-feature
```

---

### PASO 3: Crear Pull Request (1min)
1. Ve a GitHub → Banner **"Compare & pull request"**
2. Título: `Implementar nueva feature. Fixes AB#22`
3. Descripción:
   ```
   ## Cambios
   - Feature implementada

   Fixes AB#22
   ```
4. Click **Create pull request**

---

### PASO 4: Mergear PR (2min)
1. Click **Merge pull request** → **Confirm merge**
2. Ve a pestaña **Actions** → Muestra pipeline corriendo
3. Mientras corre, explica:
   - **Build**: *"Compila y ejecuta tests"*
   - **Deploy**: *"Despliega a producción"*
4. Espera a que termine (1-2 min) ⏱️

---

### PASO 5: Mostrar ticket en Done (30seg)
1. Una vez que el pipeline termine ✅
2. Ve a **Azure Boards** → **Refresca (F5)**
3. Muestra que el ticket se movió a **Done** automáticamente
4. Di: *"El sistema actualizó el estado del ticket automáticamente"*

---

## Puntos clave para explicar

- **CI/CD**: Automatiza testing y deployment
- **Ahorro de tiempo**: Sin intervención manual
- **Trazabilidad**: Cada cambio vinculado a un ticket
- **Calidad**: Tests automáticos previenen errores

---

## Si algo falla

- Pipeline no corre → Verifica que **mergeaste** el PR (no solo crearlo)
- Ticket no se mueve → Muévelo manualmente y di: *"Esto se automatiza con la integración"*

---

¡Buena suerte! 🚀
