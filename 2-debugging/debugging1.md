
### Exercice de Debugging JavaScript: Calcul des Ventes Hebdomadaires

  ** Introduction au problème:**
    Vous êtes en charge du développement d'un script pour calculer les ventes totales hebdomadaires pour un magasin. Le script doit ajouter un bonus de 50 EUR pour les jours où les ventes dépassent 400 EUR. Une fois les bonus ajoutés, vous devez trier les montants de vente par ordre décroissant avant de calculer le total final. 

Le script initial a été écrit, mais il ne fonctionne pas correctement et produit des résultats incohérents. 

Votre tâche est d'identifier et de corriger les erreurs dans le script pour garantir que le total calculé est correct.

** Script à corriger:**

```javascript 
const weeklySales = [
    { date: "2023-04-01", amount: 200 },
    { date: "2023-04-02", amount: 450 },
    { date: "2023-04-03", amount: 300 },
    { date: "2023-04-04", amount: 650 },
    { date: "2023-04-05", amount: 475 },
    { date: "2023-04-06", amount: 350 },
    { date: "2023-04-07", amount: 220 }
];

function calculateTotalSales(sales) {
    // Applying a bonus for days with sales over $400
    sales.forEach(sale => {
        if (sale.amount > 400) {
            sale.amount += 50;
        }
    });

    // Sorting sales by amount
    sales.sort((a, b) => a.amount - b.amount);

    // Calculating total sales
    let total = 0;
    sales.forEach(sale => {
        total += sale.amount;
    });
    return total;
}

const totalSales = calculateTotalSales(weeklySales);
console.log("Total sales for the week:", totalSales);`
```

**Instructions :**

1. lire et comprendre le code fourni.
2.  identifier les erreurs qui empêchent le script de fonctionner correctement (erreurs syntaxiques, logiques ou de conception)
3.  corriger les erreurs identifiées
4.  exécuter le script modifié pour vérifier que le total des ventes est correct.