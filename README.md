# Frigate-On-ProxMox
Frigate is a locally hosted, open-source NVR designed for real-time object detection using AI. By leveraging Proxmox, you can ensure a robust, isolated, and scalable home security setup.

  Proxmox Virtualization:


Resource Isolation: Run Frigate in a dedicated Linux Container (LXC) to ensure its high-intensity processing doesn't interfere with other home lab services.

Hardware Pass-through: Easily pass through Google Coral TPUs and Intel/AMD/Nvidia GPUs for efficient AI inference and video transcoding.

Snapshots & Backups: Create instant restore points before making major configuration changes or updates.

AI-Powered Detection: Uses TensorFlow Lite to detect people, cars, and other specific objects, drastically reducing false motion alerts.

Local processing ensures your video data never leaves your private network.

Streamlined Workflow: Easy configuration via YAML.

Low-latency live viewing and quick playback of recorded events.


  Getting Started on Proxmox


Prepare the Host: Ensure your Proxmox host has the necessary drivers for your Coral TPU or GPU.

Create a Container: We recommend an LXC for lower overhead and easier hardware pass-through.

Install Docker inside LXC: To avoid manual installation of complex dependencies, use docker inside of your LXC to take advantage of the pre-configured Docker Image directly supported by frigate developers.

Configure Frigate: Mount your storage drives for 24/7 recordings and map your config.yml.

Launch: Start the service and access the web UI via your Proxmox node's IP.
