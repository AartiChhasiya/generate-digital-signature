# generate-digital-signature

## To access thi library you need to pass following details:
  > 1. Primary HSM IP
  > 2. Secondary HSM IP
  > 3. Port
  > 4. Index
  > 5. Input message

	inputMessage := `{"MachineName":"ABCD-XYZ-5986","UserName":"foo@bar","Timestamp":"2018-10-17T11:12:05.4212206+05:30"}`
	
	var hsmPrimaryIP uint32 = [long-ip]
	var hsmSecondaryIP uint32 = [long-ip]
	var hsmPort int = [port-number]
	var signKeyIndex int16 = [some-index]

	hsm := hsmutil.NewHSMSigningWithPort(hsmPrimaryIP, hsmSecondaryIP, hsmPort, signKeyIndex)
	hsm.GenerateSignature(inputMessage)
