# Making Locally-Trusted Development Certificates

Install **[mkcert]**(https://github.com/FiloSottile/mkcert) and follow the instructions on their Github.

mkcert automatically creates and installs a local CA in the system root store, and generates locally-trusted certificates. 
mkcert does not automatically configure servers to use the certificates, though, that's up to you.
