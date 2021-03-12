> Movie (title, year, studioName, president, presAddr)
>   FD1: title, year -> studioName
>   FD2: studioName -> president
>   FD3: president -> presAddr
>   Key: {title, year}

Violations: FD2 FD3

---

- taking FD2
S1 (studioName, president) is in BCNF
S2 (studioName, title, year, presAddr)
  FD1: title, year -> studioName
  FD2: studioName -> presAddr
  Key: {title, year}

Violations: FD2

- taking FD2
S3 (studioName, presAddr) is in BCNF
S4 (studioName, title, year) is in BCNF

**Res**: S1, S3, S4
