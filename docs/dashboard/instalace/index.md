---
title: Návod k instalaci aplikace FaceApp
description: Docs intro
---



## Instalace potřebného softwaru na počítač

Pro vývoj a nasazení aplikace je třeba splňovat všechny [předpoklady](https://jakubkacerek.github.io/BP-DOCS/dashboard/p%C5%99edpoklady/) a nainstalovat následující nástroje:

###  Flutter SDK

- Stáhněte si nejnovější verzi [Flutter SDK](https://docs.flutter.dev/get-started/install) z oficiální stránky.
- Rozbalte stažený archiv do vhodného adresáře (např. `C:\Flutter`).
- Přidejte cestu k `flutter/bin` do systémové proměnné [PATH](https://superuser.com/questions/284342/what-are-path-and-other-environment-variables-and-how-can-i-set-or-use-them).
- Ověřte instalaci příkazu v terminálu: `flutter doctor`. Tento příkaz zkontroluje, zda jsou všechny závislosti (např. Android SDK) přítomny.

###  Android Studio

- Stáhněte si a nainstalujte [Android Studio](https://developer.android.com/studio) z oficiální stránky.
- Během instalace zvolte instalaci Android SDK a emulátoru.
- V Android Studio otevřete "SDK Manager" a ujistěte se, že je nainstalování nejnovější verze Android SDK (např. API 33).
- Nastavte [proměnnou prostředí](https://superuser.com/questions/284342/what-are-path-and-other-environment-variables-and-how-can-i-set-or-use-them) `ANDROID_HOME` na cestu k Android SDK 
(např. `C:\Users\Uživatel\AppData\Local\Android\Sdk`).

## 1. Stažení zdrojového kódu

- Otevřete terminál a přejděte do adresáře, kam chcete projekt uložit 
(např. `cd ~/Projects`).
- Naklonujte repozitář s kódem příkazem:
```shell
git clone https://github.com/JakubKacerek/BP_TUL_25
```
- Přejděte do složky projektu:
```shell
cd BP_TUL_25
```
## 2. Instalace závislostí
- Nainstalujte závislosti projektu příkazem:
```shell
flutter pub get
```
## 3. Nastavení pro telefon
- Ujistěte se, že máte mobilní telefon připojený USB kabelem k počítači.
- Zkontrolujte, že na telefonu máte zaplé "Možnosti pro vývojáře" a "USB ladění" ukázáno v [předpokladech aplikace](https://jakubkacerek.github.io/BP-DOCS/dashboard/p%C5%99edpoklady/).

## 4. Sestavení aplikace na telefon
- Ověřte, zda je telefon rozpoznán příkazem:
```shell
flutter devices
```
Měl by se zobrazit vaše zařízení (např. `android-arm`).

- Sestavte a nainstalujte aplikaci na telefon příkazem:
```shell
flutter run
```
Tento příkaz spustí aplikaci přímo na připojeném zařízení. Pokud je vše správně nastaveno, uvidíte živý náhled kamery.

### (Volitelné) Vytvoření APK pro Android

- Spusťte příkaz:
```shell
flutter build apk
```
- Poté nainstalujte generovaný `.apk` soubor příkazem:
```shell
flutter install
```

## 5. Ověření funkčnosti

- Po instalaci otevřete aplikaci na telefonu.
- Ujistěte se, že kamera funguje a detekuje obličeje nebo text podle zvolených nastavení (detekce obličejů, rozpoznávání obličejů, OCR).
- Pokud narazíte na problémy (např. chybí oprávnění kamery), povolte je přímo v nastavení aplikace v telefonu.

## 6. Řešení problémů

- Pokud `flutter doctor` hlásí chybějící závislosti, nainstalujte je podle doporučení (např. Android SDK).
- Při chybách s USB laděním zkontrolujte kabel a ovladače zařízení.
- Pro další pomoc se podívejte do dokumentace [Flutteru](https://docs.flutter.dev/) nebo [repozitáře](https://github.com/JakubKacerek/BP_TUL_25) aplikace.