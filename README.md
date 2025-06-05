import socket
import whois

def identify_website_info(website):
    try:
        # Get IP address
        ip_address = socket.gethostbyname(website)
        
        # Get domain information
        domain_info = whois.whois(website)
        creation_date = domain_info.creation_date
        
        return ip_address, creation_date
    except Exception as e:
        return str(e)

if __name__ == "__main__":
    website = input("Enter the website or social media URL: ")
    ip, created = identify_website_info(website)
    print(f"IP Address: {ip}")
    print(f"Creation Date: {created}")
    
