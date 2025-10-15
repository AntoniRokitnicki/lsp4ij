# Wskazówki dla współtwórców

Poniżej znajdziesz opis wszystkich dostępnych punktów rozszerzeń udostępnianych przez wtyczkę. Dokument ten pomaga szybko zorientować się, które mechanizmy możesz zaimplementować w swoim module IntelliJ.

## Punkty rozszerzeń

- **`com.redhat.devtools.lsp4ij.installerTaskFactory`** – umożliwia rejestrowanie własnych fabryk zadań instalacyjnych odpowiedzialnych za przebieg instalacji serwera językowego. Dzięki temu możesz dostosować proces pobierania, rozpakowywania lub konfiguracji serwera do specyficznych potrzeb.

- **`com.redhat.devtools.lsp4ij.server`** – pozwala zadeklarować fabrykę serwera językowego, którą klient wykorzysta do uruchomienia i powiązania serwera z IDE. Tu definiujesz logikę startu, parametry oraz sposób komunikacji.

- **`com.redhat.devtools.lsp4ij.languageMapping`** – wiąże obiekt `Language` z IntelliJ (i opcjonalnie dopasowanie dokumentu lub `languageId`) z wcześniej zdefiniowanym serwerem językowym. Dzięki temu wskazujesz, dla jakich języków ma być uruchamiany konkretny serwer.

- **`com.redhat.devtools.lsp4ij.fileTypeMapping`** – mapuje dany `FileType` z IntelliJ na serwer językowy w sytuacjach, gdy nie istnieje dedykowana klasa `Language`. Sprawdza się dla ogólnych typów plików.

- **`com.redhat.devtools.lsp4ij.fileNamePatternMapping`** – pozwala podpiąć serwer językowy na podstawie wzorca nazwy pliku (np. `*.less`), zachowując jednocześnie kolorowanie składni oparte na TextMate.

- **`com.redhat.devtools.lsp4ij.semanticTokensColorsProvider`** – umożliwia dostarczenie własnego mapowania tokenów na `TextAttributesKey` wykorzystywanego w semantycznym podświetlaniu składni.

- **`com.redhat.devtools.lsp4ij.debugAdapterServer`** – dodaje możliwość podpięcia fabryki serwera Debug Adapter Protocol, aby udostępnić niestandardowe scenariusze uruchamiania i debugowania.

## Dodatkowe uwagi

Dokument ma charakter informacyjny i nie nakłada dodatkowych ograniczeń stylistycznych. Stosuj ogólne zasady formatowania oraz dobre praktyki IntelliJ.
