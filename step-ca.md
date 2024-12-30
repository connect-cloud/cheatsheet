
### Check if service is running
sudo systemctl status step-ca.service

### Generate a leaf cert:
step ca certificate onzincert.test.nl test2.crt test2.key --kty EC --curve P-384 --not-after=8760h --san 10.555.1.1 --san test.connect-cloud.com
