#basic
An **IDoc (Intermediate Document)** is a proprietary standardized data format from SAP that enables the exchange of master as well as transactional business data (e.g. article master data, orders). 

The data provision and transmission within the source system is decoupled.  The transfer of the 
data is done asynchronously by a push request which can be repeated in case of unsuccessful data sent. 
### Key Concepts:

- **Structure**: An Idoc consists of a control record, data records, and status records. Each part plays a crucial role in managing information flows—containing metadata, the actual data, and processing status respectively.
- **Types**: IDocs are categorized as Basic and Extended Idocs. Basic Idocs handle standard processes, whereas Extended Idocs accommodate custom needs by adding additional fields.
- **Processing**: IDocs operate through a process called ALE (Application Link Enabling), which manages distribution, replication, and synchronization of data across systems.
- **Status & Monitoring**: IDocs have specific statuses like 'created', 'ready for dispatch', 'success', or 'error', allowing users to track their journey and troubleshoot problems.

It consists of a control record and several data and status records. The control record contains details of the dispatch (e.g. type & recipient), status records the status of the processing within SAP and the data contains the actual payload of the transmission. See also the example at the bottom.
### Usage
There are various ways of transmitting IDocs to a destination, such as tRFC, via XML file and sending XML via HTTP. In general only sending XML by HTTP should be used while creating and moving files should be avoided.
### Resources

#website Introduction, Administration & Development of IDocs [IDoc Interface/ALE | SAP Help Portal](https://help.sap.com/docs/SAP_S4HANA_ON-PREMISE/8f3819b0c24149b5959ab31070b64058/4ab074b6aa3a1997e10000000a421937.html?locale=en-US)

### Example
```
< ORDERS04 >
	< IDOC >
	"=>  control record"
		< EDI_DC40 >
			< DOCNUM > 0000002795406728 </ DOCNUM >
			< MESTYP > ORDERS </ MESTYP >
			< SNDPOR > SAPQS4 </ SNDPOR >
			< SNDPRT > LS </ SNDPRT >
			< RCVPOR > GKR_SAPDE </ RCVPOR >
			...
		</ EDI_DC40 >
    "=>  data records / Head"		
		< E1EDK01 >
			< CURCY > EUR </ CURCY >
			< BSART > UB </ BSART >
			< BELNR > 4546701413 </ BELNR >
			..
		</ E1EDK01 >
...
    "=>  data records / Positions"
		< E1EDP01 >
			< POSEX > 00010 </ POSEX >
			< MENGE > 45.000 </ MENGE >
			< MENEE > KO </ MENEE >
			< MATKL > FMV </ MATKL >
			< WERKS > 0210 </ WERKS >
			< E1EDP20 >
				< WMENG > 45.000 </ WMENG >
				< EDATU > 20250829 </ EDATU >
			</ E1EDP20 >
			< E1EDP19 >
				< IDTNR > 000000000000000917 </ IDTNR >
				< KTEXT > TC Feine Milde 250gx2x9 Vakum </ KTEXT >
			</ E1EDP19 >
		</ E1EDP01 >
```