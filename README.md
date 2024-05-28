# WHOIS Lookup Script

This project features a Python script designed to perform WHOIS lookups for domain names. WHOIS is a protocol used to query databases that store the registered users or assignees of an Internet resource, such as a domain name or an IP address block. This script connects to the WHOIS server, sends a query, and retrieves information about the specified domain name.

## Features

- **Socket Connection**: Utilizes Python's `socket` library to establish a connection with the WHOIS server.
- **Query Execution**: Sends a domain query to the WHOIS server and receives the response.
- **Data Retrieval**: Extracts and decodes the response from the WHOIS server to present detailed information about the domain, including registrant details, registration dates, and domain status.
- **Example Usage**: Includes a demonstration of how to use the script to query the domain "google.com".

## Installation

1. **Clone the repository**:
    ```sh
    git clone https://github.com/yourusername/whois-lookup-script.git
    cd whois-lookup-script
    ```

2. **Ensure Python is installed**:
    - This script requires Python 3.x. You can download and install the latest version from [python.org](https://www.python.org/downloads/).

## Usage

1. Save the script to a `.py` file, for example, `whois_lookup.py`.

2. Run the script in a terminal or command prompt:
    ```sh
    python whois_lookup.py
    ```

3. You can also modify the script to query different domains. For example, replace `"google.com"` with any other domain name in the script.

## Example

Here's an example of how to use the script to perform a WHOIS lookup for `google.com`:

```python
import socket

def whois_lookup(domain: str):
    s = socket.socket(socket.AF_INET, socket.SOCK_STREAM)
    s.connect(("whois.iana.org", 43))
    s.send(f"{domain}\r\n".encode())
    response = s.recv(4096).decode()
    s.close()
    return response

# Example usage
print(whois_lookup("google.com"))


Once you typed it in and ran the script it,

when you open the google chrome website it should be pinned in your google web browser

https://github-production-user-asset-6210df.s3.amazonaws.com/160808546/334012437-9a5627d3-cbdb-443c-a623-32fab653f589.png?X-Amz-Algorithm=AWS4-HMAC-SHA256&X-Amz-Credential=AKIAVCODYLSA53PQK4ZA%2F20240528%2Fus-east-1%2Fs3%2Faws4_request&X-Amz-Date=20240528T070816Z&X-Amz-Expires=300&X-Amz-Signature=027659316585d142eb5de8b12b2b8d234933e829ceb3b7b1342fe27575a00386&X-Amz-SignedHeaders=host&actor_id=160808546&key_id=0&repo_id=806434263
