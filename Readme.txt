Versions:

  Java Client 11.08.000.128
  JRE 1.8.0 Update 222-b10 X64 OpenJDK
  ELO OCR Service 10.17.101.003
  ELO Macros Java Client 11.00.014
  PDF Printer (GS) 2.0.0.42
  PDF Printer PrintArchive (GS) 2.0.0.42
  PDF Printer Dropzone (GS) 2.0.0.42
  Tiff Printer 5.00.020
  ELO Dropzone 11.00.010


The installation can be configured by modifying the file name. 
The name is assembled according to the following pattern:

  <Prefix>_<Language>_<Flags>_<http/https><ServerName>_<Port>_<OcrPort>_<RepositoryName>_<RepositoryProfileName>.exe

  You can choose whatever prefix you want here.

  Only the RepositoryProfileName may contain an underscore. If other parts of the file name contain an '_', the 
  default separator has to be changed. To do so, add or change the 'Separator' entry in the Language.ini file 
  under the section [SETTINGS]. Don't forget to change also the separator in the file name. 

  f.e. 
    [SETTINGS]
    Separator=_
  change to
    [SETTINGS]
    Separator=|

  and the file name to
  <Prefix>|<Sprache>|<Flags>|<http/https><ServerName>|<Port>|<OcrPort>|<ArchiveName>|<ArchiveProfileName>.exe



  Flags:
    J - Java Client
    C - OCR
    W - Word macro
    I - PowerPoint macro
    E - Excel macro
    O - Outlook Add-in
    A - Install the macros for ALL users
    P - PDF Printer
    Z - Pdf Printer Dropzone
    Q - PDF Printer Print&Archive
    T - TIFF Printer
    N - Internet Explorer Connector
    D - Windows Explorer Connector
    F - Mozilla Firefox
    G - Google Chrome
    S - Silent Installation

  Example: SetupJC_DE_JWEOPT_http_eloserver_9090_10345_elo_repository ELO.exe

  Http/https: You can select secure hypertext transfer protocol if your server supports it.
 

  Example: SetupJC_DE_JWEOPT_http_eloserver_9090_10345_elo_repository ELO.exe



The installation directory can be defined using the "INSTALLDIR" parameter.

Example: <Prefix>_<Language>_<Flags>_<http/https><ServerName>_<Port>_<OcrPort>_<RepositoryName>_<RepositoryProfileName>.exe INSTALLDIR="%ProgramFiles%\ELO"

The following additional parameters can be used for Java memory reservation:
  XMX (maximum size of Java heap memory, e.g. 1000m)
  XMS (starting size of Java heap memory, e.g. 200m)

  Example: <Prefix>_<Language>_<Flags>_<http/https><ServerName>_<Port>_<OcrPort>_<RepositoryName>_<RepositoryProfileName>.exe XMX="800m"

If a barcode serial number is available, it can be provided using the "SERNO_BARCODE" parameter.
  Example: <Prefix>_<Language>_<Flags>_<http/https><ServerName>_<Port>_<RepositoryName>_<RepositoryProfileName>.exe SERNO_BARCODE="123"


Information about the ELO PDF Printer (GS)
The installer attempts to load the required postscript for the PDF converter (ELO PS Converter.msi) to the PdfPrinter directory and execute it from there. If the file is stored there, it will be used. If the download fails, the temporary folder is used. 


Information about OCR
The ELO OCR service (client) cannot be used on a terminal server and cannot be installed on one. In this case, the OCR server is used. 



