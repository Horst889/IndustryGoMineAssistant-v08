# Industry GO Mine Assistant v0.8

Main fixes in v0.8:
- final confirmation dialog now detects the large blue **Bauen** button visually, so it no longer depends only on OCR/Accessibility text
- calibrated fallback for the supplied 945x2048 phone layout moved to approximately x=61%, y=68%
- if the confirmation dialog is still visible, the assistant retries the final button several times instead of returning to probing
- status messages identify whether the final confirmation used visual detection, OCR, Accessibility, or the calibrated fallback
- v0.7 safety logic remains: probing points must stay inside the detected 96 m green area, including mine radius and safety margin
- 20 m / 26 m / 32 m mine sizes are still read from the build dialog
- final build remains blocked unless `kein Nexus-Verbrauch` is recognized

Recommended test: stand still and observe a single complete cycle through the second Bauen button and the `Mine gebaut` confirmation before using continuous automation.
