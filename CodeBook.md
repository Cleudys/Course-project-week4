# Course-project-week4

Libro de códigos para el proyecto del curso de obtención y limpieza de datos de Coursera

El conjunto de datos al que pertenece este libro de códigos se encuentra en el archivo tidy_data.txt de este repositorio.

Consulte el archivo README.md de este repositorio para obtener información general sobre este conjunto de datos.

La estructura del conjunto de datos se describe en la sección Datos, sus variables se enumeran en la sección Variables y las transformaciones que se llevaron a cabo para obtener el conjunto de datos en base a los datos de origen se presentan en la sección Transformaciones.

Datos

El archivo de datos tidy_data.txt es un archivo de texto que contiene valores separados por espacios.

La primera fila contiene los nombres de las variables, que se enumeran y describen en la sección Variables, y las siguientes filas contienen los valores de estas variables.

Variables

Cada fila contiene, para un tema y una actividad determinados, 79 mediciones de señales promediadas.

Identificadores 

tema

Identificador de sujeto, número entero, varía de 1 a 30.

actividad

Identificador de actividad, cadena con 6 valores posibles:

CAMINAR: el sujeto caminaba WALKING_UPTAIRS: el sujeto caminaba arriba WALKING_DOWNSTAIRS: el sujeto caminaba abajo SENTADO: el sujeto estaba sentado DE PIE: el sujeto estaba de pie ACOSADO: el sujeto estaba acostado Promedio de medidas

Todas las medidas son valores de coma flotante, normalizados y acotados dentro de [-1,1].

Antes de la normalización, las medidas de aceleración (variables que contienen acelerómetro) se realizaron en g (9,81 ms⁻²) y las medidas de giroscopio (variables que contienen giroscopio) se realizaron en radianes por segundo (rad.s⁻¹).

Las magnitudes de las señales tridimensionales (variables que contienen Magnitud) se calcularon utilizando la norma euclidiana.

Las medidas se clasifican en dos dominios:

Señales en el dominio del tiempo (variables con el prefijo timeDomain), que resultan de la captura de señales sin procesar del acelerómetro y del giroscopio.

Señales en el dominio de la frecuencia (variables prefijadas por el dominio de la frecuencia), resultantes de la aplicación de una Transformada Rápida de Fourier (FFT) a algunas de las señales en el dominio del tiempo.

Señales en el dominio del tiempo

Aceleración corporal promedio en el dominio del tiempo en las direcciones X, Y y Z:

timeDomainBodyAccelerometerMeanX timeDomainBodyAccelerometerMeanY timeDomainBodyAccelerometerMeanZ Desviación estándar de la aceleración del cuerpo en el dominio del tiempo en las direcciones X, Y y Z:

timeDomainBodyAccelerometerStandardDeviationX timeDomainBodyAccelerometerStandardDeviationY timeDomainBodyAccelerometerStandardDeviationZ Aceleración de gravedad promedio en el dominio del tiempo en las direcciones X, Y y Z:

timeDomainGravityAccelerometerMeanX timeDomainGravityAccelerometerMeanY timeDomainGravityAccelerometerMeanZ Desviación estándar de la aceleración de la gravedad en el dominio del tiempo en las direcciones X, Y y Z:

timeDomainGravityAccelerometerStandardDeviationX timeDomainGravityAccelerometerStandardDeviationY timeDomainGravityAccelerometerStandardDeviationZ Promedio de la aceleración del cuerpo en el dominio del tiempo (derivación de la aceleración en el tiempo) en las direcciones X, Y y Z:

timeDomainBodyAccelerometerJerkMeanX timeDomainBodyAccelerometerJerkMeanY timeDomainBodyAccelerometerJerkMeanZ Desviación estándar del tirón de aceleración del cuerpo en el dominio del tiempo (derivación de la aceleración en el tiempo) en las direcciones X, Y y Z:

timeDomainBodyAccelerometerJerkStandardDeviationX timeDomainBodyAccelerometerJerkStandardDeviationY timeDomainBodyAccelerometerJerkStandardDeviationZ Velocidad angular media del cuerpo en el dominio del tiempo en las direcciones X, Y y Z:

timeDomainBodyGyroscopeMeanX timeDomainBodyGyroscopeMeanY timeDomainBodyGyroscopeMeanZ Desviación estándar de la velocidad angular del cuerpo en el dominio del tiempo en las direcciones X, Y y Z:

timeDomainBodyGyroscopeStandardDeviationX timeDomainBodyGyroscopeStandardDeviationY timeDomainBodyGyroscopeStandardDeviationZ Jerk de velocidad angular del cuerpo en el dominio del tiempo promedio (derivación de la velocidad angular en el tiempo) en las direcciones X, Y y Z:

timeDomainBodyGyroscopeJerkMeanX timeDomainBodyGyroscopeJerkMeanY timeDomainBodyGyroscopeJerkMeanZ Desviación estándar del tirón de la velocidad angular del cuerpo en el dominio del tiempo (derivación de la velocidad angular en el tiempo) en las direcciones X, Y y Z:

timeDomainBodyGyroscopeJerkStandardDeviationX timeDomainBodyGyroscopeJerkStandardDeviationY timeDomainBodyGyroscopeJerkStandardDeviationZ Promedio y desviación estándar de la magnitud de la aceleración corporal en el dominio del tiempo:

timeDomainBodyAccelerometerMagnitudeMean timeDomainBodyAccelerometerMagnitudeStandardDeviation Promedio y desviación estándar de la magnitud de la aceleración de la gravedad en el dominio del tiempo:

timeDomainGravityAccelerometerMagnitudeMean timeDomainGravityAccelerometerMagnitudeStandardDeviation Promedio y desviación estándar de la magnitud en el dominio del tiempo del tirón de aceleración corporal (derivación de la aceleración en el tiempo):

timeDomainBodyAccelerometerJerkMagnitudeMean timeDomainBodyAccelerometerJerkMagnitudeStandardDeviation Promedio y desviación estándar de la magnitud en el dominio del tiempo de la velocidad angular del cuerpo:

timeDomainBodyGyroscopeMagnitudeMean timeDomainBodyGyroscopeMagnitudeStandardDeviation Promedio y desviación estándar de la magnitud en el dominio del tiempo del tirón de la velocidad angular del cuerpo (derivación de la velocidad angular en el tiempo):

timeDomainBodyGyroscopeJerkMagnitudeMean timeDomainBodyGyroscopeJerkMagnitudeStandardDeviation Frecuencias-dominio señales

Aceleración corporal media en el dominio de la frecuencia en las direcciones X, Y y Z:

FrequencyDomainBodyAccelerometerMeanX FrequencyDomainBodyAccelerometerMeanY FrequencyDomainBodyAccelerometerMeanZ Desviación estándar de la aceleración del cuerpo en el dominio de frecuencia en las direcciones X, Y y Z:

FrequencyDomainBodyAccelerometerStandardDeviationX FrequencyDomainBodyAccelerometerStandardDeviationY FrequencyDomainBodyAccelerometerStandardDeviationZ Promedio ponderado de los componentes de frecuencia de la aceleración del cuerpo en el dominio de frecuencia en las direcciones X, Y y Z:

FrequencyDomainBodyAccelerometerMeanFrequencyX FrequencyDomainBodyAccelerometerMeanFrequencyY frecuenciaDomainBodyAccelerometerMeanFrequencyZ Jerk de aceleración del cuerpo en el dominio de frecuencia promedio (derivación de la aceleración en el tiempo) en las direcciones X, Y y Z:

FrequencyDomainBodyAccelerometerJerkMeanX FrequencyDomainBodyAccelerometerJerkMeanY FrequencyDomainBodyAccelerometerJerkMeanZ Desviación estándar del tirón de aceleración del cuerpo en el dominio de la frecuencia (derivación de la aceleración en el tiempo) en las direcciones X, Y y Z:

FrequencyDomainBodyAccelerometerJerkStandardDeviationX FrequencyDomainBodyAccelerometerJerkStandardDeviationY FrequencyDomainBodyAccelerometerJerkStandardDeviationZ Promedio ponderado de los componentes de frecuencia del tirón de aceleración del cuerpo en el dominio de la frecuencia (derivación de la aceleración en el tiempo) en las direcciones X, Y y Z:

FrequencyDomainBodyAccelerometerJerkMeanFrequencyX FrequencyDomainBodyAccelerometerJerkMeanFrequencyY frecuenciaDomainBodyAccelerometerJerkMeanFrequencyZ Velocidad angular media del cuerpo en el dominio de frecuencia en las direcciones X, Y y Z:

FrequencyDomainBodyGyroscopeMeanX FrequencyDomainBodyGyroscopeMeanY frecuenciaDomainBodyGyroscopeMeanZ Desviación estándar de la velocidad angular del cuerpo en el dominio de frecuencia en las direcciones X, Y y Z:

FrequencyDomainBodyGyroscopeStandardDeviationX FrequencyDomainBodyGyroscopeStandardDesviationY FrequencyDomainBodyGyroscopeStandardDeviationZ Promedio ponderado de los componentes de frecuencia de la velocidad angular del cuerpo en el dominio de la frecuencia en las direcciones X, Y y Z:

FrequencyDomainBodyGyroscopeMeanFrequencyX frecuenciaDomainBodyGyroscopeMeanFrequencyY frecuenciaDomainBodyGyroscopeMeanFrequencyZ Promedio, desviación estándar y promedio ponderado de los componentes de frecuencia de la magnitud del dominio de frecuencia de la aceleración corporal:

FrequencyDomainBodyAccelerometerMagnitudeMean FrequencyDomainBodyAccelerometerMagnitudeStandardDeviation FrequencyDomainBodyAccelerometerMagnitudeMeanFrequency Promedio, desviación estándar y promedio ponderado de los componentes de frecuencia de la magnitud del dominio de frecuencia del tirón de aceleración corporal (derivación de la aceleración en el tiempo):

FrequencyDomainBodyAccelerometerJerkMagnitudeMean FrequencyDomainBodyAccelerometerJerkMagnitudeStandardDeviation FrequencyDomainBodyAccelerometerJerkMagnitudeMeanFrequency Promedio, desviación estándar y promedio ponderado de los componentes de frecuencia de la magnitud del dominio de frecuencia de la velocidad angular del cuerpo:

FrequencyDomainBodyGyroscopeMagnitudeFrecuencia mediaDomainBodyGyroscopeMagnitudeStandardDesviación frecuenciaDomainBodyGyroscopeMagnitudeMeanFrequency Promedio, desviación estándar y promedio ponderado de los componentes de frecuencia de la magnitud del dominio de frecuencia del tirón de velocidad angular del cuerpo (derivación de la velocidad angular en el tiempo):

frecuenciaDomainBodyGyroscopeTirónMagnitudFrecuencia mediaDominioCuerpoGiroscopioTirónMagnitudEstándarFrecuencia de desviaciónDominioCuerpoGiroscopioJerkMagnitudMediaFrecuencia

Transformaciones

El archivo zip que contiene los datos de origen se encuentra en https://d396qusza40orc.cloudfront.net/getdata%2Fprojectfiles%2FUCI%20HAR%20Dataset.zip .

Se aplicaron las siguientes transformaciones a los datos de origen:

Los conjuntos de entrenamiento y prueba se fusionaron para crear un conjunto de datos.

Las medidas de la desviación media y estándar (es decir, las señales que contienen las cadenas media y std) se extrajeron para cada medida y las demás se descartaron.

Los identificadores de actividad (originalmente codificados como números enteros entre 1 y 6) fueron reemplazados por nombres descriptivos de actividades (ver la sección de Identificadores).

Los nombres de las variables se reemplazaron con nombres de variables descriptivos (por ejemplo, tBodyAcc-mean () - X se expandió a timeDomainBodyAccelerometerMeanX), utilizando el siguiente conjunto de reglas: Se eliminaron los caracteres especiales (es decir, (,) y -). expandido a FrequencyDomain y timeDomain respectivamente. Acc, Gyro, Mag, Freq, mean y std fueron reemplazados por Acelerómetro, Giroscopio, Magnitud, Frecuencia, Media y Desviación Estándar respectivamente. Reemplazado (supuestamente incorrecto según el archivo features_info.txt de la fuente) BodyBody con Body.