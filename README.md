# Furlong Feed Handler

A C++20 market-data processing and order-book reconstruction system designed to explore efficient event ingestion, deterministic state updates, and reliable recovery from missing or invalid messages.

## Overview

Market-data systems transform streams of exchange events into a continuously updated view of market state. This project explores the engineering challenges involved in processing those events correctly and efficiently.

## Core Features

* **Event Processing:** Handle order additions, modifications, cancellations, and trade events.
* **Order Book Reconstruction:** Maintain bid and ask levels from incremental updates.
* **Sequence Validation:** Detect missing, duplicated, and out-of-order messages.
* **Snapshot Recovery:** Restore state from snapshots and resume incremental processing.
* **Deterministic Replay:** Reproduce market state from a recorded event stream.
* **Performance Measurement:** Measure message throughput and processing latency.

## Technical Stack

* C++20
* CMake
* GoogleTest
* Google Benchmark
* Python for test-data generation and analysis

## Architecture

1. Message decoder
2. Sequence validator
3. Event processor
4. Order-book state manager
5. Snapshot and recovery module
6. Replay and benchmarking tools

## Correctness and Performance

The system will be evaluated using:

* Unit and property-based tests
* Snapshot-versus-replay consistency checks
* Malformed-message and sequence-gap tests
* Messages processed per second
* Processing-latency distributions
* Memory usage under sustained workloads

## Build and Run

Build instructions and executable commands will be documented as the implementation evolves.

## Project Status

Under development. Performance results and supported message formats will be documented after implementation and testing.

## Scope

This is an educational market-data processing system. It is not an exchange-certified feed handler and does not connect to a live exchange by default.
