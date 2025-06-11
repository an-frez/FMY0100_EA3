# Resumen de archivos
El objectivo de este proyecto aprendizaje de maquinas es predecir la columna TimeAlive, o sea el tiempo que el juagador se mantiene con vida.
## dataclean.ipynb
Se limpia la data del archivo csv para ser utilizada de manera uniforme en los modelos.
## regresionesLineales.ipynb
Se realiza regresion lineal simple y multiple.
### Regresiones Lineal Simples
Se mide el score de las variables una por una en el valor de X.
```
--- X Value: Team
Mean Squared Error: 2.0758363260893503e+32
Mean Absolute Error: 9670052169057276.0
R2 Score: -3.7494494603995676e-05

--- X Value: MatchWinner
Mean Squared Error: 2.0814393851168777e+32
Mean Absolute Error: 9653322649385564.0
R2 Score: 7.380687393165886e-05

--- X Value: FirstKillTime
Mean Squared Error: 2.062389571350766e+32
Mean Absolute Error: 9640219181989336.0
R2 Score: -5.320805317010624e-06

--- X Value: RoundKills
Mean Squared Error: 2.0680842734158747e+32
Mean Absolute Error: 9649417225966152.0
R2 Score: 0.0015546148583204245

--- X Value: RoundStartingEquipmentValue
Mean Squared Error: 2.0693607585735837e+32
Mean Absolute Error: 9679429522691942.0
R2 Score: 0.001395510792436827

--- X Value: TeamStartingEquipmentValue
Mean Squared Error: 2.053340199091427e+32
Mean Absolute Error: 9613016975513946.0
R2 Score: 0.0009878344495640734
```
### Regresion Lineal Multiple
Se mide el score de la regresion, esta vez incorporando todas las variables anteriormente mencionadas.
```
Mean Squared Error: 2.020635716262942e+32
Mean Absolute Error: 9571605918587778.0
R2 Score: 0.0005735093491271437
```
## MAQUINA_SOPORTE_VECTORES.ipynb
Se intenta utilizar el modelo de la maquina de soporte de vectores, pero por tema de RAM insuficiente el modelo no se puede ejecutar. Se intenta acotar y simplificar la data pero aun asi el modelo no es entrenable. Queda pendiente restructurar la data de mejor manera.
## Arbol.ipynb
Se realiza un Grid Search para encontrar el mejor modelo dentro de los parametros establecidos.
Los parametros encontrados para este modelo son los siguientes.
```
{'criterion': 'poisson',
'max_depth': np.int64(7),
'max_features': 'sqrt',
'min_samples_split': np.int64(11)}
```
El score del arbol se muestra a continuacion.
```
MSE:  2.066242928024247e+32
MAE:  9805315589116804.0
R^2:  0.020515029858900302
```
## FOREST.ipynb
Se realiza un Grid Search para encontrar el mejor modelo dentro de los parametros establecidos.
Los parametros encontrados para este modelo son los siguientes.
```
{'max_depth': np.int64(6),
'max_features': 'sqrt',
'max_leaf_nodes': np.int64(20),
'min_samples_split': np.int64(6),
'n_estimators': 200}
```
El score del arbol se muestra a continuacion.
```
MSE:  1.9931296825487322e+32
MAE:  9493997887812936.0
R^2:  0.009990560678114768
```
# Conclusion
De todos los modelos, el arbol de decicion y el random forest fueron los que mejor resultados dieron. Pero, poniendolo en perspectiva, ni uno de los modelos fue muy certero. 
