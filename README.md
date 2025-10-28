# ERD sistem E-Wallet
ERD yang di buat untuk membuat gambaran untuk struktur database yang akan di buat untuk sistem e-wallet

## Preview
```mermaid
erDiagram

user{
    string nama
    string nomer_hp
    string alamat
    string pin
}

wallet{
    string nama
    int jumlah_uang
}

transaksi{
    string nomer_transaksi
    int jumlah_uang
    date transaksi_dibuat
    string nama_user
    string nama_bank
    string tipe
}


history{
    string name
    string nomer_history
    date tanggal_transaksi
    int jumlah_uang
}
user||--o|wallet : masuk
wallet||--o{transaksi : membuat
wallet||--o{history : data
```