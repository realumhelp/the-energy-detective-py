# TEDpy

Unofficial library for reading from The Energy Detective power meters

This library supports the TED5000 and TED6000 devices.

It is based on @realumhelp's [ted6000py](https://github.com/realumhelp/ted6000py), Home Assistant's ted5000 implementation, and @gtdiehl and @jesserizzo's [envoy_reader](https://github.com/gtdiehl/envoy_reader/).

## Usage

```python
from tedpy import createTED

HOST = 'ted6000'

# Use asyncio to deal with the async methods
reader = await createTED(HOST)
await reader.update()
reader.print_to_console()
```