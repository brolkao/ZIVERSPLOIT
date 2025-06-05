import socket
import whois
import sys

def identify_website_info(website):
    try:
        # Get IP address
        ip_address = socket.gethostbyname(website)
        
        # Get creation date
        domain_info = whois.whois(website)
        creation_date = domain_info.creation_date
        
        print(f"Website: {website}")
        print(f"IP Address: {ip_address}")
        print(f"Creation Date: {creation_date}")
    except Exception as e:
        print(f"Error: {e}")

if __name__ == "__main__":
    if len(sys.argv) != 2:
        print("Usage: python identify.py <website>")
    else:
        identify_website_info(sys.argv[1])
