# uTest Academy · Testing Tools · 04: Mobile Device Logs

| Campo / Field | Valor / Value |
|---|---|
| Plataforma / Platform | uTest (Applause) |
| Situação / Status | ✅ Concluído · quiz 6 de 6 / Completed · quiz 6 of 6 |
| Fonte / Source | [uTest Academy: Mobile Device Logs](https://platform.utest.com/academy/tracks/6/courses/40/lessons/android-device-logs) (login) |
| Referências / References | [Android SDK Platform-Tools (adb)](https://developer.android.com/tools/releases/platform-tools) · [Android: logcat](https://developer.android.com/tools/logcat) · [iMazing](https://imazing.com/) |

## Android (adb)
⚠️ 🇧🇷 Use sempre **adb** (Platform-Tools) ou o **Android Studio**. **Nunca** apps como Syslog ou CatLog. 🇺🇸 Always **adb** or Android Studio; **never** apps like Syslog/CatLog.

**Antes / Prerequisites**
1. 🇧🇷 Toque **7×** no **Número da versão** → **Opções do desenvolvedor** → **Depuração USB**. 🇺🇸 Tap **Build number 7×** → enable **USB debugging**.
2. 🇧🇷 Celular desbloqueado e ligado ao computador por **cabo USB que transfere dados**; marque **"Sempre permitir deste computador"**. 🇺🇸 Unlocked, **data USB cable**, "Always allow".
3. 🇧🇷 Se o antivírus bloquear o adb, coloque-o como exceção. 🇺🇸 Add adb to antivirus exceptions if blocked.

~~~mermaid
flowchart LR
    A[Abrir terminal na pasta<br/>platform-tools<br/>Open terminal] --> B[adb logcat -c<br/>limpar / clear]
    B --> C[Reproduzir o bug<br/>do início ao fim<br/>Reproduce the bug]
    C --> D[adb logcat -d -v time > log.txt]
    D --> E[Anexar log.txt<br/>Attach log.txt]
~~~

| Sistema / OS | Comando / Command |
|---|---|
| **Windows** | <code>adb logcat -c</code> → reproduzir → <code>adb logcat -d -v time &gt;.\log.txt</code> |
| **macOS / Linux** | <code>./adb logcat -c</code> → reproduzir → <code>./adb logcat -d -v time &gt;./log.txt</code> |
| **Recomendado / Recommended** | <code>adb logcat -v threadtime &gt;.\log.txt</code> → reproduzir → <code>Ctrl + C</code> para parar / to stop |

- 🇧🇷 Log grande demais? Feche outros apps e limpe com <code>adb logcat -c</code> antes de abrir o app. Erro no adb? <code>adb kill-server</code> e repita. 🇺🇸 Too large → close apps, clear first; errors → <code>adb kill-server</code>.

## iOS
| Método / Method | 🇧🇷 Como | 🇺🇸 How |
|---|---|---|
| **iMazing** (Windows e macOS) | conectar o iPhone → **Show Device Console** → limpar → reproduzir → Pause → **Save** em .txt. Grátis para uso pessoal e educacional; uso comercial pode exigir licença. Alternativas só para Windows: 3uTools, iTools. | Show Device Console → clear → reproduce → save .txt |
| **App Console** (só macOS) | escolher o iPhone → **All messages** → Clear → reproduzir → <code>Command+A</code>, <code>Command+C</code> → colar no TextEdit em **texto simples** → salvar .txt | Console app → copy → TextEdit plain text → .txt |
| **libimobiledevice** (Linux) | <code>idevicesyslog &#124; tee uTest_log.txt</code> → reproduzir → <code>Ctrl + C</code> | |

## Crash logs do iOS / iOS crash logs
🇧🇷 Mostram **como o app fechou** e o código de cada thread na hora do crash. 🇺🇸 Show how the app terminated.
- 🇧🇷 **No aparelho:** reproduza o crash → Ajustes → Privacidade → **Análise e Melhorias** → **Dados de Análise** → relatório com o nome do app e o horário → compartilhar → anexar o **.ips**. 🇺🇸 Settings → Privacy → Analytics & Improvements → Analytics Data → share the **.ips**.
- 🇧🇷 **iTunes** (Windows ou macOS anterior ao Catalina): sincronizar e pegar o .log, .crash ou .ips na pasta CrashReporter/MobileDevice. 🇺🇸 Via iTunes sync folder.

## Quiz comentado / Commented quiz (6/6)
1. Como ativar as Opções do desenvolvedor / Enable Developer Options → ✅ **Tocar 7 vezes no Número da versão**.
2. "Use um app como Syslog para logs do Android" → ✅ **Falso / False** (use adb ou Android Studio).
3. Programa que NÃO serve para log de iOS / NOT for iOS logs → ✅ **Android Studio** (iMazing, iTools e 3uTools servem).
4. O que precisa para log de Android no Windows / Needed on Windows → ✅ **Todas**: Platform-Tools, cabo USB de dados, computador Windows e aparelho Android.
5. Comando correto / Correct command → ✅ <code>adb logcat -d -v time &gt;.\log.txt</code>.
6. App Android: qual método? / Android app: which method? → ✅ **SDK Platform-Tools** (❌ remote debugging do Chrome é para **site**, não app).
