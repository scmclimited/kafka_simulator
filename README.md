# Kafka Producer Module

This module provides a Kafka-compatible interface for sending logs to a Kafka topic. It supports both simulated log output (for testing environments) and real Kafka cluster communication via `kafka-python`.

## Features

- `KafkaProducerSimulated`: writes logs to a local `.jsonl` file as a substitute for Kafka.
- `KafkaProducerReal`: sends logs to an actual Kafka topic using the `kafka.KafkaProducer` interface.
- CLI-compatible initialization via the main project entrypoint (`main.py`).
- Strictly typed and compatible with Pyright's `strict` mode.
- Includes base class `BaseKafkaProducer` for abstract producer behavior.

## Directory Structure

kafka_producer/
├── kafka_producer.py      # Main logic for simulated and real Kafka producers

## Usage Overview

This module is designed to be imported and used via the project’s main CLI runner:

`https://github.com/scmclimited/random_log_generator/blob/main/main.py`

```bash
python main.py --mode stream --count 10 --use-kafka-sim true
