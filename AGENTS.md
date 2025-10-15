# Instrukcje dla rozszerzeń LSP4IJ

Poniższy plik opisuje wszystkie punkty rozszerzeń dostępne w pluginie. Zastosuj te informacje, jeżeli planujesz je implementować.

## com.redhat.devtools.lsp4ij.installerTaskFactory
Rejestruje własne fabryki zadań instalacyjnych wykorzystywanych podczas procesu instalacji serwera językowego. Pozwala rozszerzyć i dostosować kolejne kroki instalacji.

## com.redhat.devtools.lsp4ij.server
Deklaruje fabrykę serwera językowego, dzięki której klient potrafi uruchomić oraz skonfigurować połączenie z wybranym LSP.

## com.redhat.devtools.lsp4ij.languageMapping
Mapuje obiekt `Language` IntelliJ (opcjonalnie z dopasowaniem dokumentów lub `languageId`) na wcześniej zdefiniowaną konfigurację serwera językowego.

## com.redhat.devtools.lsp4ij.fileTypeMapping
Powiązuje konkretny `FileType` IntelliJ z wybranym serwerem językowym w sytuacji, gdy nie istnieje dedykowany obiekt `Language`.

## com.redhat.devtools.lsp4ij.fileNamePatternMapping
Łączy wzorce nazw plików (np. `*.less`) z serwerem językowym, jednocześnie zachowując istniejące kolorowanie oparte na TextMate.

## com.redhat.devtools.lsp4ij.semanticTokensColorsProvider
Udostępnia własną mapę przypisującą tokeny do `TextAttributesKey`, co pozwala dostosować podświetlanie semantyczne.

## com.redhat.devtools.lsp4ij.debugAdapterServer
Podłącza fabrykę deskryptora Debug Adapter Protocol, umożliwiając przygotowanie niestandardowych doświadczeń uruchamiania i debugowania.
