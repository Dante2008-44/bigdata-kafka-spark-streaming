# Análisis de Datos en Tiempo Real con Apache Kafka y Spark Streaming

Proyecto de Big Data - Curso 202016911  
Universidad Nacional Abierta y a Distancia (UNAD)

## Descripción

Este proyecto implementa un pipeline de procesamiento de datos en tiempo real utilizando Apache Kafka y Apache Spark Structured Streaming, siguiendo el Anexo 3 del curso.

Se simulan datos de sensores (temperatura y humedad) que se envían a un topic de Kafka llamado `sensor_data`. Luego, Spark Streaming procesa estos datos en ventanas de tiempo de 1 minuto y calcula el promedio de temperatura y humedad por cada sensor.

## Archivos del proyecto

- `kafka_producer.py`: Script productor que genera y envía datos simulados de sensores a Kafka.
- `spark_streaming_consumer.py`: Script consumidor que lee los datos desde Kafka y realiza el análisis en tiempo real con Spark Streaming.
- `README.md`: Este archivo con las instrucciones.

## Requisitos previos

- Máquina virtual con Hadoop y Spark configurados (Anexos 1 y 2)
- Apache Kafka instalado
- Librería `kafka-python` instalada (`pip3 install kafka-python`)

## Instrucciones de ejecución

### 1. Iniciar ZooKeeper y Kafka

```bash
sudo /opt/Kafka/bin/zookeeper-server-start.sh /opt/Kafka/config/zookeeper.properties &
sudo /opt/Kafka/bin/kafka-server-start.sh /opt/Kafka/config/server.properties &