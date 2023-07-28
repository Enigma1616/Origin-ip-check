# Origin-ip-check
FInd Origin IP using domain name
import socket

def get_origin_ip(domain):
    try:
        ip = socket.gethostbyname(domain)
        return ip
    except socket.gaierror:
        return None

def find_origin_ip():
    domain = input("Enter the testing domain: ")
    origin_ip = get_origin_ip(domain)

    if origin_ip:
        print(f"The origin IP of {domain} is: {origin_ip}")
    else:
        print(f"Failed to retrieve the origin IP of {domain}")

find_origin_ip()
