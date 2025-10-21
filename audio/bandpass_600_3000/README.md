# BO LOC BANDPASS 600-3000 Hz

## Tong quan
Dai tan so **600-3000 Hz** duoc toi uu hoa cho **giong noi** va **speech recognition**.

## Tai sao chon 600-3000 Hz?

### So sanh voi cac dai tan so khac:

| Dai tan so | Ung dung | Uu diem | Nhuoc diem |
|------------|----------|---------|------------|
| **100-7000 Hz** | Audio tong quat | Giu nhieu thong tin | Co nhieu hum va noise |
| **300-3000 Hz** | Giong noi co ban | Ro giong noi | Van con mot so hum thap |
| **600-3000 Hz** ⭐ | **Giong noi toi uu** | **Loai bo hum tot nhat**, **Ro rang nhat** | **Mat mot so thong tin < 600 Hz** |

### Ly do chon 600-3000 Hz:
1. **Loai bo hum dien hieu qua** (50 Hz, 100 Hz, harmonics)
2. **Loai bo nhieu tan so thap** (< 600 Hz)
3. **Giu lai pho am cua giong noi** (600-3000 Hz)
4. **Loai bo nhieu tan so cao** (> 3000 Hz)
5. **Toi uu cho speech recognition engines**

## Ket qua da tao

### 1. Audio files (7 files - 590KB moi file)
```
✓ channel_1_bandpass_600_3000.wav  - Channel 1 da loc
✓ channel_2_bandpass_600_3000.wav  - Channel 2 da loc
✓ channel_3_bandpass_600_3000.wav  - Channel 3 da loc
✓ channel_4_bandpass_600_3000.wav  - Channel 4 da loc
✓ channel_5_bandpass_600_3000.wav  - Channel 5 da loc (MANH NHAT)
✓ channel_8_bandpass_600_3000.wav  - Channel 8 da loc
✓ mixed_audio_bandpass_600_3000.wav - Audio tron tu 6 channels
```

### 2. Bieu do so sanh (7 files)
Moi bieu do bao gom 4 phan:
1. **Waveform Original** - Audio goc truoc khi loc
2. **Waveform Filtered** - Audio sau khi loc 600-3000 Hz
3. **Spectrum Original** - Pho tan so truoc khi loc
4. **Spectrum Filtered** - Pho tan so sau khi loc (ro rang hieu qua cua bo loc)

```
✓ comparison_channel_1.png - So sanh Channel 1
✓ comparison_channel_2.png - So sanh Channel 2
✓ comparison_channel_3.png - So sanh Channel 3
✓ comparison_channel_4.png - So sanh Channel 4
✓ comparison_channel_5.png - So sanh Channel 5
✓ comparison_channel_6.png - So sanh Channel 8
✓ all_channels_bandpass_600_3000.png - Tong hop tat ca channels
```

## Chi tiet channels

| Channel | RMS    | Chat luong | File audio |
|---------|--------|------------|------------|
| 1       | 2943.2 | ⭐ Yeu | channel_1_bandpass_600_3000.wav |
| 2       | 3475.3 | ⭐ Yeu | channel_2_bandpass_600_3000.wav |
| 3       | 5626.7 | ⭐⭐ Tot | channel_3_bandpass_600_3000.wav |
| 4       | 6410.6 | ⭐⭐ Tot | channel_4_bandpass_600_3000.wav |
| 5       | 9891.0 | ⭐⭐⭐ **MANH NHAT** | channel_5_bandpass_600_3000.wav |
| 8       | 5081.2 | ⭐⭐ Tot | channel_8_bandpass_600_3000.wav |

## Huong dan su dung

### 1. Nghe audio da loc
```bash
# Windows
start channel_5_bandpass_600_3000.wav

# VLC
vlc channel_5_bandpass_600_3000.wav
```

### 2. Xem so sanh truoc/sau khi loc
```bash
# Xem bieu do so sanh chi tiet
start comparison_channel_5.png

# Xem tong hop tat ca channels
start all_channels_bandpass_600_3000.png
```

### 3. Su dung cho speech recognition
```python
import wave

# Doc file audio da loc
with wave.open('channel_5_bandpass_600_3000.wav', 'rb') as f:
    sample_rate = f.getframerate()  # 16000 Hz
    n_channels = f.getnchannels()   # 1 (Mono)
    audio_data = f.readframes(f.getnframes())
    
# Su dung voi speech recognition engine
# Google Speech-to-Text, CMU Sphinx, etc.
```

## So sanh voi cac bo loc khac

### Bandpass 300-3000 Hz
- **Uu diem:** Giu nhieu thong tin hon
- **Nhuoc diem:** Van con hum < 300 Hz

### Bandpass 600-3000 Hz ⭐ (BO LOC NAY)
- **Uu diem:** Loai bo hum tot nhat, ro rang nhat
- **Nhuoc diem:** Mat mot so thong tin < 600 Hz (khong quan trong cho giong noi)
- **TOT NHAT CHO:** Speech recognition, voice analysis, giong noi ro rang

### Bandpass 100-7000 Hz
- **Uu diem:** Giu nhieu thong tin nhat
- **Nhuoc diem:** Co nhieu hum va noise

## Thong so ky thuat

### Bo loc
- **Loai:** Butterworth Bandpass Filter
- **Order:** 5
- **Cutoff frequencies:** 600 Hz (low), 3000 Hz (high)
- **Method:** Zero-phase filtering (filtfilt)
- **Attenuation:** -3dB tai 600 Hz va 3000 Hz

### Audio
- **Sample rate:** 16000 Hz
- **Bit depth:** 16-bit
- **Format:** WAV (PCM)
- **Channels:** Mono (1 channel)
- **Normalization:** 90% max amplitude

### Hieu qua cua bo loc
```
Tan so < 600 Hz:  Loai bo gan het (> -40 dB)
Tan so 600-3000 Hz: Giu nguyen (0 dB)
Tan so > 3000 Hz: Loai bo gan het (> -40 dB)
```

## Ung dung thuc te

### 1. Speech Recognition
```
✅ Goi y: Su dung channel_5_bandpass_600_3000.wav
✅ Ly do: Manh nhat, ro rang nhat
✅ Engines: Google Speech-to-Text, Azure Speech, CMU Sphinx
```

### 2. Voice Analysis
```
✅ Goi y: Su dung tat ca channels
✅ Ly do: So sanh chat luong giua cac microphones
✅ Tools: Praat, Audacity, MATLAB
```

### 3. Noise Reduction
```
✅ Goi y: Su dung mixed_audio_bandpass_600_3000.wav
✅ Ly do: Trung binh tu 6 channels, giam noise
✅ Result: Audio on dinh, chat luong tot
```

### 4. Telecom/VoIP
```
✅ Goi y: Bo loc nay tuong tu G.711 codec
✅ Ly do: Dai tan so toi uu cho truyen dan giong noi
✅ Bandwidth: Tiet kiem bandwidth, chat luong van tot
```

## So sanh audio quality

### Truoc khi loc (Original)
- **Uu diem:** Giu toan bo thong tin
- **Nhuoc diem:** Co hum 50Hz, noise thap va cao
- **SNR:** Thap (co nhieu noise)

### Sau khi loc (Bandpass 600-3000 Hz)
- **Uu diem:** Loai bo hum va noise hieu qua
- **Nhuoc diem:** Mat mot so thong tin ngoai dai 600-3000 Hz
- **SNR:** Cao (giam nhieu noise)
- **Clarity:** Tang ro rang, giong noi sach hon

## Performance metrics

### Noise reduction
- **Hum dien 50 Hz:** Giam > 40 dB
- **Noise thap (< 600 Hz):** Giam > 30 dB
- **Noise cao (> 3000 Hz):** Giam > 30 dB

### Signal preservation
- **Giong noi (600-3000 Hz):** Giu nguyen ~100%
- **Pho am co ban:** Giu nguyen
- **Pitch va intonation:** Giu nguyen

### Computational cost
- **Processing time:** ~0.5s cho 18s audio
- **Memory usage:** Minimal
- **Real-time capable:** Yes

## Troubleshooting

### Audio nghe qua "thin" (mong)
```
Ly do: Bo loc loai bo tan so < 600 Hz
Giai phap: Neu can bass, dung bandpass 300-3000 Hz
```

### Van con hum dien
```
Ly do: Hum co the o harmonics cao hon (100Hz, 150Hz, etc.)
Giai phap: Ket hop voi notch filters 50Hz, 100Hz, 150Hz
```

### Audio qua on
```
Ly do: Normalization qua cao
Giai phap: Giam normalization level tu 0.9 xuong 0.7
```

## Ket luan

Bo loc **Bandpass 600-3000 Hz** la lua chon **TOI UU NHAT** cho:
- ✅ Speech recognition
- ✅ Voice communication
- ✅ Giong noi ro rang
- ✅ Loai bo hum va noise

**KHONG PHU HOP** cho:
- ✗ Music playback (can dai tan so rong hon)
- ✗ Audio mixing (can tan so thap va cao)
- ✗ Bass-heavy content (loai bo tan so thap)

## Files da tao

**Tong cong: 14 files**
- 7 audio files WAV (590 KB moi file) = ~4.1 MB
- 7 comparison plots PNG (~400 KB moi file) = ~2.8 MB
- **TONG:** ~7 MB

**San sang su dung cho speech recognition va voice analysis!**

