# Psuedocode1
MPT1


BEGIN
		DECLARE consumer_no AS INTEGER
		DECLARE consumer_name AS string
		DECLARE no_of_units AS INTEGER

		INITIALIZE consumer_no=0
		INITIALIZE no_of_units=0

END

/****************************************************************************

*Module Name 		: accept consumer_info()
*Input Parameters 	: none
*Return Type		: void
*Author 		: Sayani Hazra
*Creation Date 		: 8-December-2016
*Description		: accepting and checking validity and displaying the inputs

******************************************************************************/

SUB accept_info()
	
		PROMPT "Enter the Consumer number" AND STORE IN consumer_no
	
		IF isvalid(consumer_no) THEN
			PRINT "Consumer number entered is" + consumer_no

		END IF
		
		IF(Consumer_no<=0 )
			RAISE ConsumerNumberNotValid("Consumer Number cannot be 0 or less than 0");

		END IF



		PROMPT "Enter the Consumer name" AND STORE IN consumer_name
		PROMPT "The Consumer name entered is" +consumer_name

		PROMPT "Enter the number of units" AND STORE IN no_of_units


		IF(no_of_units <=0)
			RAISE NumberOfUnitsNotValid("Units consumed cannot be less than 0")

		END IF

		IF(IsDigit(no_of_units))

		PRINT"The number of units entered is "+ no_of_units

		ELSE

			RAISE NumberOfUnitsNotValid("Units consumed cannot be less than 0")
		END IF

	EXCEPTION

		WHEN notvalidconsumer_no
		THEN PRINT errormessage;
		
		WHEN notvalidno_of_units
		THEN PRINT errormessage;

END SUB



		



	
