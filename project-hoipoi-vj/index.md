
# HoiPoi Audio-Reactive VJ Production

> **Roles:** Creative Technologist / Computer Graphics Engineer / Live Visuals Developer

![Languages](https://img.shields.io/badge/Languages-C%23%20%2F%20HLSL-239120)
![Core](https://img.shields.io/badge/Core-FFT%20Audio%20Analysis-555555)
![Domain](https://img.shields.io/badge/Domain-Live%20VJ%20%2F%20Audio--Reactive%20Visuals-ff4d6d)
![Timeline](https://img.shields.io/badge/Timeline-May%202025-0f766e)

## Executive Summary

### 日本語

高円寺 HoiPoi で開催されたイベント向けに、DJ 音源へリアルタイムに反応する VJ ビジュアルを制作しました。FFT で音声を低域・中域・高域に分け、各帯域の変化を使って映像の動き、色、エフェクトの強さを変化させました。

### English

I created an audio-reactive VJ system for a live event at HoiPoi in Koenji, Tokyo. The system used FFT analysis to split DJ audio into low-, mid-, and high-frequency bands, then used those values to control visual motion, color, and effect intensity in real time.

## Documentation & Gallery Grid

<table width="100%">
  <tr>
    <td width="50%"><img src="./photos/IMG1.jpg" alt="HoiPoi VJ venue output 01" width="100%"/></td>
    <td width="50%"><img src="./photos/IMG2.jpg" alt="HoiPoi VJ venue output 02" width="100%"/></td>
  </tr>
  <tr>
    <td width="50%"><img src="./photos/IMG3.jpg" alt="HoiPoi VJ venue output 03" width="100%"/></td>
    <td width="50%"><img src="./photos/IMG4.jpg" alt="HoiPoi VJ venue output 04" width="100%"/></td>
  </tr>
</table>

## Technical Stack

| Layer | Implementation |
|---|---|
| Audio analysis | FFT-based frequency band extraction |
| Runtime control | C# |
| Visual synthesis | HLSL shaders |
| Output | Live VJ visuals for HoiPoi event projection |

## Technical Core & Architectural Highlights

### Audio Analysis

- Used FFT analysis to read the DJ audio as low-, mid-, and high-frequency bands.
- Connected each band to simple visual parameters such as scale, movement, color, and intensity.
- Smoothed the values enough to keep the response stable during live playback.

### Visual System

- Built the control layer in C# and the visual response with HLSL shaders.
- Generated the visuals in real time instead of playing back a fixed video.
- Tuned the output for HoiPoi's venue atmosphere and projection conditions.

### Live Production

- Kept the setup simple and stable for an event environment.
- Adjusted response strength so the visuals followed the DJ set without overpowering it.
- Captured the venue output through still documentation.

## Technical Pipeline Diagram

```text
[DJ Audio Input]
       |
       v
[FFT Analysis]
       |
       +--> [Low Band]  -> Bass response / scale
       +--> [Mid Band]  -> Motion response
       +--> [High Band] -> Texture / effect response
       |
       v
[C# Parameter Mapping]
       |
       v
[HLSL Visual Shader]
       |
       v
[HoiPoi Venue Output]
```