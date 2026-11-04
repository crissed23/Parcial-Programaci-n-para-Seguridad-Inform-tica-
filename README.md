# Parcial-Programaci-n-para-Seguridad-Inform-tica-

for ($i = 1; $i -le 3; $i++) {
    $fecha = Get-Date

    if ($i % 2 -eq 0) {
        Write-Host "Iteración $i (Par): Verificación secundaria de red a las $fecha" -ForegroundColor Cyan
    } else {
        Write-Host "Iteración $i (Impar): Diagnóstico principal de adaptadores a las $fecha" -ForegroundColor Yellow
    }

    Get-NetAdapter | Where-Object Status -eq 'Up'
    Write-Host "--------------------------------------------------"
}

Write-Host "El monitoreo ha concluido con éxito." -ForegroundColor Green
