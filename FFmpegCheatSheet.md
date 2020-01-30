## Lossless video encoding with APPLE ProRes from images
`ffmpeg -i %02d.png -c:v prores_ks -profile:v 3 -c:a pcm_s16le -vf fps=30 output.mov`

## LowRes(360p) vs HighRes(720p) side by side demo
`ffmpeg -y -ss 00:00:00 -t 00:00:10 -i pengsoo.webm -filter_complex '[v]scale=640x360[int1],[v]scale=1280x720[int2],[int1][int2]scale2ref[test][base];[test][base]vstack[vid]' -map [vid] -c:v prores_ks pengsoo_360_720.mov`
