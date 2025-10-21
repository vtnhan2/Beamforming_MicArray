# TOM TAT KET QUA LOC AUDIO TAT CA CHANNELS

## Thong tin chung
- **File input:** audio/original_8channels.pcm
- **Duration:** 18.46 giay
- **Sample rate:** 16000 Hz
- **Channels co audio:** 6/8 (channels 1, 2, 3, 4, 5, 8)
- **Channels silent:** 2/8 (channels 6, 7)

## Ket qua xu ly

### Tong quat
- **Tong so channels da xu ly:** 6
- **Tong so file audio da tao:** 36 (6 channels x 6 loai bo loc)
- **Tong so bieu do:** 14 (12 bieu do cho tung channel + 2 bieu do tong hop)
- **Tong cong files:** 50

### Chi tiet tung channel

#### Channel 1 (RMS: 2943.2)
**Thu muc:** `channel_1/`
**Audio files:**
1. `channel_1_original.wav` - Audio goc khong loc
2. `channel_1_bandpass_100_7000.wav` - Loc dai 100-7000 Hz
3. `channel_1_bandpass_300_3000.wav` - Loc dai 300-3000 Hz (giong noi)
4. `channel_1_highpass_300.wav` - Loc thong cao 300 Hz
5. `channel_1_lowpass_5000.wav` - Loc thong thap 5000 Hz
6. `channel_1_notch_50hz.wav` - Loai bo hum 50 Hz

**Bieu do:**
- `waveform_channel_1.png` - So sanh waveform cac bo loc
- `spectrum_channel_1.png` - So sanh pho tan so cac bo loc

---

#### Channel 2 (RMS: 3475.3)
**Thu muc:** `channel_2/`
**Audio files:**
1. `channel_2_original.wav`
2. `channel_2_bandpass_100_7000.wav`
3. `channel_2_bandpass_300_3000.wav`
4. `channel_2_highpass_300.wav`
5. `channel_2_lowpass_5000.wav`
6. `channel_2_notch_50hz.wav`

**Bieu do:**
- `waveform_channel_2.png`
- `spectrum_channel_2.png`

---

#### Channel 3 (RMS: 5626.7)
**Thu muc:** `channel_3/`
**Audio files:**
1. `channel_3_original.wav`
2. `channel_3_bandpass_100_7000.wav`
3. `channel_3_bandpass_300_3000.wav`
4. `channel_3_highpass_300.wav`
5. `channel_3_lowpass_5000.wav`
6. `channel_3_notch_50hz.wav`

**Bieu do:**
- `waveform_channel_3.png`
- `spectrum_channel_3.png`

---

#### Channel 4 (RMS: 6410.6)
**Thu muc:** `channel_4/`
**Audio files:**
1. `channel_4_original.wav`
2. `channel_4_bandpass_100_7000.wav`
3. `channel_4_bandpass_300_3000.wav`
4. `channel_4_highpass_300.wav`
5. `channel_4_lowpass_5000.wav`
6. `channel_4_notch_50hz.wav`

**Bieu do:**
- `waveform_channel_4.png`
- `spectrum_channel_4.png`

---

#### Channel 5 (RMS: 9891.0) ⭐ MANH NHAT
**Thu muc:** `channel_5/`
**Audio files:**
1. `channel_5_original.wav`
2. `channel_5_bandpass_100_7000.wav`
3. `channel_5_bandpass_300_3000.wav`
4. `channel_5_highpass_300.wav`
5. `channel_5_lowpass_5000.wav`
6. `channel_5_notch_50hz.wav`

**Bieu do:**
- `waveform_channel_5.png`
- `spectrum_channel_5.png`

**Ghi chu:** Channel nay co am thanh manh nhat (RMS cao nhat)

---

#### Channel 8 (RMS: 5081.2)
**Thu muc:** `channel_8/`
**Audio files:**
1. `channel_8_original.wav`
2. `channel_8_bandpass_100_7000.wav`
3. `channel_8_bandpass_300_3000.wav`
4. `channel_8_highpass_300.wav`
5. `channel_8_lowpass_5000.wav`
6. `channel_8_notch_50hz.wav`

**Bieu do:**
- `waveform_channel_8.png`
- `spectrum_channel_8.png`

---

## Bieu do tong hop

### 1. `all_channels_comparison.png`
So sanh waveform cua tat ca 6 channels (audio goc)
- Hien thi 1 giay dau cua moi channel
- De dang nhin thay channel nao manh/yeu
- Channel 5 co amplitude cao nhat

### 2. `all_channels_spectrum.png`
So sanh pho tan so cua tat ca 6 channels
- Hien thi phan bo nang luong theo tan so
- Giup nhan dien nhieu va tan so chu yeu
- De so sanh chat luong audio giua cac channels

---

## Cac loai bo loc da ap dung

### 1. Original (Khong loc)
- **Muc dich:** Luu audio goc de so sanh
- **Khi nao dung:** Can audio day du khong xu ly

### 2. Bandpass 100-7000 Hz
- **Muc dich:** Giu lai dai tan so am thanh chu yeu
- **Loai bo:** Nhieu tan so thap (<100 Hz) va cao (>7000 Hz)
- **Khi nao dung:** Xu ly audio tong quat, loai bo hum va nhieu cao
- **Tot nhat cho:** Hau het ung dung audio thong thuong

### 3. Bandpass 300-3000 Hz
- **Muc dich:** Toi uu hoa cho giong noi
- **Loai bo:** Tat ca tan so ngoai dai giong noi
- **Khi nao dung:** Speech recognition, voice processing
- **Tot nhat cho:** Phan tich giong noi, nhan dien tu

### 4. Highpass 300 Hz
- **Muc dich:** Loai bo nhieu tan so thap
- **Loai bo:** Hum dien, nhieu background tan so thap
- **Khi nao dung:** Audio co nhieu hum dien hoac nhieu thap
- **Tot nhat cho:** Lam sach audio co nhieu background

### 5. Lowpass 5000 Hz
- **Muc dich:** Loai bo nhieu tan so cao
- **Loai bo:** Tieng xit, nhieu tan so cao
- **Khi nao dung:** Audio co nhieu noise tan so cao
- **Tot nhat cho:** Lam muot audio, giam nhieu

### 6. Notch 50 Hz
- **Muc dich:** Loai bo chinh xac hum dien 50 Hz
- **Loai bo:** Chi tan so 50 Hz (hum dien chau Au/A)
- **Khi nao dung:** Phat hien hum dien ro rang
- **Tot nhat cho:** Loai bo hum dien khong anh huong den am thanh khac

---

## Huong dan su dung

### Nghe audio
```bash
# Windows Media Player
start channel_1/channel_1_bandpass_100_7000.wav

# VLC Player
vlc channel_1/channel_1_bandpass_100_7000.wav

# Audacity (de phan tich chi tiet)
audacity channel_1/channel_1_bandpass_100_7000.wav
```

### So sanh cac bo loc
1. Mo cung luc nhieu file tu cung 1 channel
2. Nghe tung file de so sanh su khac biet
3. Xem bieu do waveform va spectrum de hieu ro hon

### Chon bo loc phu hop
- **Cho speech recognition:** Dung `bandpass_300_3000.wav`
- **Cho audio tong quat:** Dung `bandpass_100_7000.wav`
- **Co nhieu hum dien:** Dung `notch_50hz.wav` hoac `highpass_300.wav`
- **Co nhieu tan so cao:** Dung `lowpass_5000.wav`

---

## Thong ke file size

### Moi file audio
- **Size:** ~590 KB (590,890 bytes)
- **Duration:** 18.46 giay
- **Format:** WAV (16-bit PCM, 16000 Hz, Mono)

### Moi bieu do waveform
- **Size:** ~850 KB
- **Resolution:** 2100 x 3000 pixels (150 DPI)
- **Format:** PNG

### Moi bieu do spectrum
- **Size:** ~430 KB
- **Resolution:** 2100 x 3000 pixels (150 DPI)
- **Format:** PNG

### Tong kich thuoc thu muc
- **Audio files:** 36 x 590 KB = ~21.2 MB
- **Waveform plots:** 12 x 850 KB = ~10.2 MB
- **Spectrum plots:** 12 x 430 KB = ~5.2 MB
- **Summary plots:** 2 x 600 KB = ~1.2 MB
- **TONG CONG:** ~38 MB

---

## Ghi chu ky thuat

### Cau hinh bo loc
- **Loai:** Butterworth filter
- **Order:** 5
- **Method:** Zero-phase filtering (filtfilt)
- **Normalization:** 90% max amplitude (0.9 x 32767)

### Uu diem cua Butterworth filter
- Dap ung tan so phang (flat frequency response)
- Khong lam nhieu pha (zero-phase)
- On dinh va de su dung

### Uu diem cua filtfilt
- Khong lam sai pha
- Bo loc 2 chieu (forward va backward)
- Quan trong cho audio de giu chat luong

---

## Ket luan

Da **THANH CONG** xu ly tat ca 6 channels co audio:
- ✅ Channel 1 (RMS: 2943) - Yeu nhat
- ✅ Channel 2 (RMS: 3475)
- ✅ Channel 3 (RMS: 5627)
- ✅ Channel 4 (RMS: 6411)
- ✅ Channel 5 (RMS: 9891) - **MANH NHAT** ⭐
- ✅ Channel 8 (RMS: 5081)

Moi channel co:
- 6 file audio voi cac loai bo loc khac nhau
- 2 bieu do (waveform va spectrum)
- Tong 8 files/channel

Tong cong 50 files da san sang su dung!

