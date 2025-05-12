# Rebar

A hardware agnostic debug probe firmware framework written in Rust.

## Motivation

Debugging is one of (if not the) the most essential parts of writing software for embedded devices, but it is also often the most confusing. The goal of this project is to make embedded debugging more accessible by making it easy to build your own debug probe, maintain existing debug probes, and support as many different hardware platforms as possible while doing so.

## Project Structure

The main `rebar` framework can be found in the [`rebar/`](https://github.com/Wtoll/Rebar/rebar) directory and contains the hardware agnostic code for writing debug probe firmware.

Hardware specific firmware implementations using `rebar` can be found in the `rebar-{platform}/` directories such as the `rebar-rp/` directory for use on the Raspberry Pi silicon family of processors. These implementations are designed to work out of the box without any need for configuration on the part of the end-user.

## Roadmap

Rebar is currently targetting the widely accessible [Raspberry Pi Debug Probe](https://www.raspberrypi.com/products/debug-probe/) hardware platform (and other RP2040 based probes) as a test case for developing the framework. That framework will then be used to add support for additional hardware platforms in the future.