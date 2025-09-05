An **IDoc (Intermediate Document)** is a proprietary standardized data format from SAP that enables the asynchronous exchange as a push of master as well as transactional business data (e.g. article master data, orders) between SAP systems and external partners.

It consists of a control record and several data and status records. The control record contains details of the dispatch (e.g. type & recipient), status records the status of the processing within SAP and the data contains the actual data of the transmission. See also the example at the bottom.

### Usage
There are various ways of transmitting IDocs to a destination, such as tRFC, via XML file and sending XML via HTTP. In general only sending XML by HTTP should be used while creating and moving files should be avoided.

IDocs provide the possibility to decouple the creation or consumption of  data within SAP from receiving / sending the data and should be used therefore used only in such use cases.
### Ressources

#website Introduction, Administration & Development of IDocs [IDoc Interface/ALE | SAP Help Portal](https://help.sap.com/docs/SAP_S4HANA_ON-PREMISE/8f3819b0c24149b5959ab31070b64058/4ab074b6aa3a1997e10000000a421937.html?locale=en-US)

### Example

```
**< ORDERS04 >**
	**< IDOC >**
	"=>  controll record"
		**< EDI_DC40 >**
			**< DOCNUM >** **0000002795406728** **</ DOCNUM >**
			**< MESTYP >** **ORDERS** **</ MESTYP >**
			**< SNDPOR >** **SAPQS4** **</ SNDPOR >**
			**< SNDPRT >** **LS** **</ SNDPRT >**
			**< RCVPOR >** **GKR_SAPDE** **</ RCVPOR >**
			...
		**</ EDI_DC40 >**
    "=>  data records / He ad"		
		**< E1EDK01 >**
			**< CURCY >** **EUR** **</ CURCY >**
			**< BSART >** **UB** **</ BSART >**
			**< BELNR >** **4546701413** **</ BELNR >**
			..
		**</ E1EDK01 >**
..
    "=>  data records / Positions"
		**< E1EDP01 >**
			**< POSEX >** **00010** **</ POSEX >**
			**< MENGE >** **45.000** **</ MENGE >**
			**< MENEE >** **KO** **</ MENEE >**
			**< MATKL >** **FMV** **</ MATKL >**
			**< WERKS >** **0210** **</ WERKS >**
			**< E1EDP20 >**
				**< WMENG >** **45.000** **</ WMENG >**
				**< EDATU >** **20250829** **</ EDATU >**
			**</ E1EDP20 >**
			**< E1EDP19 >**
				**< IDTNR >** **000000000000000917** **</ IDTNR >**
				**< KTEXT >** **TC Feine Milde 250gx2x9 Vakum** **</ KTEXT >**
			**</ E1EDP19 >**
		**</ E1EDP01 >**
```