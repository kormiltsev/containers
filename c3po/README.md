# cpppo (c3po)

## A mock Rockwell device
a simple mock Rockwell device. It responses with CIP protocol from port 44818 (CIP standard).

## Usage
The mock device should have an actual interface and IP, so container should be started with host network.

### Build
```bash
docker build -t cip-rockwell-device .
```

### Start container
```bash
docker run -it --net=host -d --name rockwell cip-rockwell-device
```
