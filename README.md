# Control Plane for CyberTom VPN

The control plane is responsible for managing all forwarding planes, issuing registration keys for users to connect to the forwarding planes, and handling various management tasks such as user device online status, node availability, and more. It is developed using Golang.

## Features
- Manages and monitors all forwarding plane nodes
- Issues and manages registration keys for user devices
- Tracks and updates the online/offline status of registered users and nodes
- Provides an API interface (to be documented)
- Scalable architecture to support growing network demands

## Build & Installation

### Prerequisites
- Golang 1.23 or later

### Build Instructions
```bash
git clone https://github.com/Cybertom-Opensource/control-plane.git
cd control-plane
go build -o control-plane
```

### Configuration
1. Create a `config` directory in the project root.
2. Place your configuration files (e.g., database connection details, server settings) in this directory.
3. Ensure all required dependencies are properly set up according to your environment.

## Running the Control Plane

```bash
./control-plane run --config ./config/your-config.yaml
```

You can also use a provided `systemd` unit file for service management:
```bash
sudo systemctl daemon-reload
sudo systemctl start control-plane
sudo systemctl enable control-plane
```

## API Reference

The API documentation is currently under development. Please check back soon for detailed API specifications and usage examples.

## Notes

- Ensure the configuration files are properly set up before starting the service.
- The control plane does not automatically configure firewall rules or network settings. You must manually set these up according to your security requirements.
- Regularly backup important data such as issued keys, user sessions, and node configurations to prevent data loss.

## Contributing

Contributions are welcome! If you'd like to contribute to this project, please fork the repository and create a pull request. Please ensure your code adheres to the existing coding style and conventions.

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.