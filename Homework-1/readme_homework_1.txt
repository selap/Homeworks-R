#Construir una matriz de 5x5 con valores aleatorios decimales en un rango de 160 a 200 que representen los pesos mensuales de 5 personas

```{r}
pesos <- matrix(data = c(161.20, 174.50, 185.30, 162.80, 170.10,
                         172.00, 195.60, 173.20, 188.50, 190.60,
                         184.70, 166.90, 162.10, 167.80, 176.60,
                         199.30, 177.15, 191.20, 180.00, 168.40,
                         169.50, 172.20, 185.40, 196.19, 173.00),
                nrow = 5, byrow = TRUE)

pesos
```

# Asignar nombres a las columnas y a las filas
```{r}
meses <- c("enero", "febrero", "marzo", "abril", "mayo")
meses
nombres <- c("Hector", "Armando", "Celso", "Arturo", "Juan")
nombres

colnames(pesos) <- meses
rownames(pesos) <- nombres

pesos
```

# Calcular el promedio mensual y agregar la fila a la matriz
```{r}
avg_mes <- colMeans(pesos)
avg_mes

prom_mes <- rbind(pesos, avg_mes)

prom_mes

```

# Calcular el promedio por persona y agregar la columna a la matriz
```{r}

avg_persona <- c(rowMeans(pesos),0)
avg_persona

promedios <- cbind(prom_mes, avg_persona)

```

#Imprimir la matriz resultante a la que se le ha llamado "promedios"

```{r}

promedios

```