# Grass Winsnip

Grass Winsnip is a Python application designed to connect to WebSocket servers using a list of SOCKS5 proxies. It performs various operations such as checking the validity of proxies, logging proxy reputations, and maintaining WebSocket connections. The application includes a scheduled task to refresh active proxies periodically.

## Prerequisites

Before you begin, ensure you have met the following requirements:

- Python 3.x
- pip (Python package installer)

## Installation

### Clone the Repository
```sh
git clone https://github.comWinnode/grass-new.git
cd grass-new
```

1. Clone the repository or download the script files.
2. Install the required Python packages by running:

    ```sh
    pip install requests==2.28.1 python-dotenv==1.0.0 eth-account==0.5.9 colorama==0.4.6 pyfiglet
    ```

## Configuration

1. Create a `config.json` file in the root directory of the project. Here is an example configuration:

    ```json
    {
      "schedule_hours": 72,
      "num_devices": 10,
      "max_active_proxies": 200,
      "use_manual_proxy": false, 
      "manual_proxy_file": "active_proxies.txt",
      "uuidproc": "aHR0cHM6Ly9yYXcuZ2l0aHVidXNlcmNvbnRlbnQuY29tL01EUC1LQ0EvYWN1cy9tYWluL3Jlc3VsdF9mb2xkZXIvYWxsLnR4dA=="
    }
    ```


2. Penjelsan config.json
    ```json
    {
      "schedule_hours": 72, # waktu restart diisi 24 untuk proxy generate auto, dan bisa di buat 72 dll tergantung proxy anda, 
      "num_devices": 10, # jumlah akun maksimal 2 untuk proxy gratis
      "max_active_proxies": 200, # maksimum proxy yg digunakan
      "use_manual_proxy": false, # apabila true maka isi proxy di active_proxies.txt 
      "manual_proxy_file": "active_proxies.txt",
      "uuidproc": "aHR0cHM6Ly9yYXcuZ2l0aHVidXNlcmNvbnRlbnQuY29tL01EUC1LQ0EvYWN1cy9tYWluL3Jlc3VsdF9mb2xkZXIvYWxsLnR4dA=="
    }
    disarankan menggunakan Proxy yg berbayar residential untuk hasil yg maksimal
    ```


2. Create a `users.txt` file containing the user IDs, one per line.
    ```json
    akun1
    akun2
    ```
## Running the Application

1. Run the application using the following command:

    ```sh
    python3 run.py
    ```

2. ### Password For those who are interested in joining our community, you can find the password at https://t.me/winsnip.

    ```sh
    Enter password: ********
    ```

3. If the password is correct, the application will start and print the ASCII banner.

## Features

- **Proxy Validation**: Checks the validity of SOCKS5 proxies by making HTTP requests.
- **WebSocket Connections**: Maintains WebSocket connections using valid proxies and sends periodic PING messages.
- **Logging**: Logs proxy reputations, connection attempts, and errors.
- **Scheduling**: Periodically refreshes the list of active proxies.

## Logging

The application uses the `loguru` library for logging. It creates two log files:

- `debug.log`: Contains debug-level logs.
- `error.log`: Contains error-level logs.

## Dependencies

- `requests`
- `asyncio`
- `json`
- `ssl`
- `uuid`
- `random`
- `concurrent.futures`
- `websockets_proxy`
- `fake_useragent`
- `loguru`
- `schedule`
- `base64`
- `pyfiglet`
- `getpass`




