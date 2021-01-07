# Response LSP

1.  [**Login**](#1-login "Login Response")
    -   [Normal Login](#normal-login "Normal Login Response")
    -   [Login with cookie](#login-with-cookie "Login with cookie Response")
2.  [**Autocomplete Dosen**](#2-autocomplete-dosen "Autocomplete Dosen Response")
3.  [**GET Dosen Name**](#3-get-dosen-name "Dosen Name Response")
4.  [**Prodi**](#4-Prodi "prodi-response")
    -   [GET Prodi Name](#get-prodi-name "Prodi Name Response")
    -   [GET All Prodi](#get-all-prodi "All Prodi Response")

## 1. Login

### Normal Login

**METHOD**

```
POST
```

**Sample Request**

```
{
    "username": "0021807008",
    "password": "Ubharaj4y4"
}
```

> Login as Lecturer/Dosen/Asesor

**Sample Response**

```
{
    "status": 1,
    "message": "success",
    "data": {
        "username": "021405022",
        "usertype": "1",
        "userid": "021405022",
        "group": "7,6",
        "prodi": "",
        "name": "Allan D. Alexander, ST, M. Kom",
        "nik": null,
        "tplhr": "Jakarta",
        "tglhr": "0000-00-00",
        "jenkel": "P",
        "hp": "081280206054",
        "email": "allan@ubharajaya.ac.id"
    }
}
```

> Login as Student/Mahasiswa/Asesi

**Sample Response**

```
{
    "status": 1,
    "message": "success",
    "data": {
        "username": "201910325153",
        "usertype": "2",
        "userid": "201910325153",
        "group": "5",
        "prodi": "61201",
        "name": "PUTRI AUDIA",
        "nik": "3275014202010022",
        "tplhr": "BEKASI",
        "tglhr": "2001-02-02",
        "jenkel": "P",
        "hp": "083877497245",
        "email": "Ptraudia74@gmail.com"
    }
}
```

> Login as Administrator

**Sample Response**

```
{
    "status": 1,
    "message": "success",
    "data": {
        "username": "LSP",
        "usertype": "8",
        "userid": "LSP",
        "group": "26",
        "prodi": "",
        "name": "Lembaga Sertifikasi Profesi P1",
        "nik": "",
        "tplhr": "",
        "tglhr": "",
        "jenkel": "",
        "hp": "",
        "email": ""
    }
}
```

### Login with cookie

**METHOD**

```
POST
```

**Sample Request**

```
{
    "username": "0021807008",
    "usertype": "1"
}
```

> Login as Lecturer/Dosen/Asesor

**Sample Response**

```
{
    "status": 1,
    "message": "success",
    "data": {
        "username": "021405022",
        "usertype": "1",
        "userid": "021405022",
        "group": "7,6",
        "prodi": "",
        "name": "Allan D. Alexander, ST, M. Kom",
        "nik": null,
        "tplhr": "Jakarta",
        "tglhr": "0000-00-00",
        "jenkel": "P",
        "hp": "081280206054",
        "email": "allan@ubharajaya.ac.id"
    }
}
```

> Login as Student/Mahasiswa/Asesi

**Sample Response**

```
{
    "status": 1,
    "message": "success",
    "data": {
        "username": "201910325153",
        "usertype": "2",
        "userid": "201910325153",
        "group": "5",
        "prodi": "61201",
        "name": "PUTRI AUDIA",
        "nik": "3275014202010022",
        "tplhr": "BEKASI",
        "tglhr": "2001-02-02",
        "jenkel": "P",
        "hp": "083877497245",
        "email": "Ptraudia74@gmail.com"
    }
}
```

> Login as Administrator

**Sample Response**

```
{
    "status": 1,
    "message": "success",
    "data": {
        "username": "LSP",
        "usertype": "8",
        "userid": "LSP",
        "group": "26",
        "prodi": "",
        "name": "Lembaga Sertifikasi Profesi P1",
        "nik": "",
        "tplhr": "",
        "tglhr": "",
        "jenkel": "",
        "hp": "",
        "email": ""
    }
}
```

## 2. Autocomplete Dosen

> enter some characters from the Lecturer NID or NAME to show the results

**METHOD**

```
POST
```

**Sample Request**

```
{
    "term": "wis"
}
```

**Sample Response**

```
{
    "status": 1,
    "message": "success",
    "data": [
        {
            "label": "0021807008 - R. Wisnu Prio Pamungkas, S.Kom., M.Kom",
            "value": "0021807008 - R. Wisnu Prio Pamungkas, S.Kom., M.Kom",
            "save": "0021807008"
        },
        {
            "label": "010803018 - M. Hanafi Darwis, Dr. Ir, SH, MM",
            "value": "010803018 - M. Hanafi Darwis, Dr. Ir, SH, MM",
            "save": "010803018"
        }
    ]
}
```

## 3. GET Dosen Name

> Get lecturer name based on NID

**METHOD**

```
POST
```

**Sample Request**

```
{
    "nid": "0021807008"
}
```

**Sample Response**

```
{
    "status": 1,
    "message": "success",
    "data": "R. Wisnu Prio Pamungkas, S.Kom., M.Kom"
}
```

## 4. Prodi

### GET Prodi Name

> Get name of prodi based on prodi code

**METHOD**

```
POST
```

**Sample Request**

```
{
    "kd_prodi": "62201"
}
```

**Sample Response**

```
{
    "status": 1,
    "message": "success",
    "data": "AKUNTANSI"
}
```

### GET ALL PRODI

> Get all prodi

**METHOD**

```
GET
```

**Sample Response**

```
{
    "status": 1,
    "message": "success",
    "data": [
        {
            "id_prodi": "5",
            "kd_prodi": "62201",
            "prodi": "AKUNTANSI",
            "kd_fakultas": "1",
            "jenjang": "S1",
            "id_sms": "a26699d1-68f5-43cd-9eea-183d02932b8a",
            "sk": "217/SK/BAN-PT/Ak-XVI/S/X/2013",
            "akreditasi": "C",
            "tahun_akreditasi": "2013",
            "tgl_kadaluarsa": "2018-10-26",
            "status_prodi": "1",
            "kaprodi": "031703067",
            "prodi_en": null
        },
        {
            "id_prodi": "7",
            "kd_prodi": "73201",
            "prodi": "PSIKOLOGI",
            "kd_fakultas": "5",
            "jenjang": "S1",
            "id_sms": "683afb04-010d-4a79-bb9e-cae295051ebb",
            "sk": "1104/SK/BAN-PT/Akred/S/IV/2017",
            "akreditasi": "C",
            "tahun_akreditasi": "2017",
            "tgl_kadaluarsa": "2022-04-18",
            "status_prodi": "1",
            "kaprodi": "051512039",
            "prodi_en": null
        }
    ]
}
```

#

[Go To TOP](#response-lsp)
