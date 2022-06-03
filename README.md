# Git-github
SUBROUTINE IDROUT
*-----------------------------------------------------------------------------
*
*-----------------------------------------------------------------------------
* Modification History :
*-----------------------------------------------------------------------------

*-----------------------------------------------------------------------------
    $INSERT I_COMMON
    $INSERT I_EQUATE
    IF COMI THEN
        IF COMI[1,1] NE '%' AND FIELD(COMI,'-',2)[1,4] NE 'LIST' THEN
            COMI='MAVERIC.TRG': COMI
    
            IF LEN(COMI) GT 30 THEN
                E='ID LENGTH RESTRICTED TO 30 CHARACTERS'
            END
        END
        ELSE
            E='CANNOT MODIFY DEFAULT ENQUIRIES'
        
        END
    END
RETURN
END

