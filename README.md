# 🎵 MP3 Tools

Una raccolta di strumenti utili per gestire, convertire e ottimizzare file MP3 (e non solo).  
Questa repository crescerà nel tempo includendo script per:

- Conversione audio/video in MP3
- Normalizzazione del volume
- Rimozione silenzi
- Gestione tag ID3
- Pulizia batch di librerie audio
- Analisi qualità e bitrate

---

## 🚀 mp3-converter.sh

Questo script permette di convertire qualsiasi file audio o video in formato **MP3** usando FFmpeg.  
Supporta sia la conversione di **un singolo file**, sia la conversione **batch** della directory corrente.

### ✨ Funzionalità

- Converte automaticamente formati comuni (wav, flac, m4a, mp4, mov, ogg, webm, avi, wma, aac…)
- Mantiene la qualità con codifica **VBR (libmp3lame)**
- Evita di riconvertire file già `.mp3`
- Elimina il file originale **solo dopo** una conversione riuscita
- Mostra un riepilogo finale
- Non richiede dipendenze extra oltre a `ffmpeg`

---

## 🎛️ RMusicConverter (Advanced Python Converter)

Uno script Python interattivo e avanzato per la conversione, l'estrazione e la riorganizzazione massiva di librerie audio e video. Funziona come una vera e propria applicazione a riga di comando (CLI) grazie ai suoi menu navigabili (State Machine).

### ✨ Funzionalità

- **Menu Interattivo (Loop):** Interfaccia guidata passo-passo. Puoi tornare al menu precedente (`B`) o uscire (`Q`) in qualsiasi momento senza interruzioni improvvise.
- **Estrazione Ricorsiva (Flatten):** Cerca tutti i file multimediali annidati in decine di sottocartelle e portali in un'unica directory centralizzata rinominata col timestamp di sistema.
- **Taglia & Incolla Sicuro:** Al termine dell'elaborazione, i file originali vengono rimossi. In caso di errore (es. corruzione del file), l'originale viene mantenuto e viene generato un `error_log.txt`.
- **Gestione Metadati Avanzata:** Scegli se mantenere i metadati originali, fare uno "strip" totale (rimuovere ogni tag ID3) o sovrascriverli inserendo un nuovo Titolo e Artista.
- **Auto-Cleanup & Sanitizzazione:** Ripulisce automaticamente i nomi dei file (rimuove parentesi, virgole, simboli strani e spazi) ed elimina le directory che rimangono vuote dopo l'estrazione dei file.
- **Smart Audio/Video Split:** Riconosce da solo se un file è audio o video. Permette l'estrazione diretta dell'audio dai video senza ricodifiche inutili (modalità `-c copy` quando possibile).

---

## 🔧 Requisiti

Per utilizzare gli strumenti di questa repository, assicurati di avere i seguenti pacchetti installati:

- `bash` (per `mp3-converter.sh`)
- `python3` (per `Rconverter`)
- `ffmpeg` (motore di conversione base per entrambi gli script)

**Installazione dipendenze di sistema:**
*Debian/Ubuntu:* ```bash
sudo apt update && sudo apt install ffmpeg python3
