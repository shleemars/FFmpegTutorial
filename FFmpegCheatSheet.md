## Lossless video encoding with APPLE ProRes from images
`ffmpeg -i %02d.png -c:v prores_ks -profile:v 3 -c:a pcm_s16le -vf fps=30 output.mov`
