# Deal

## Properties
Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**order_id** | **string** | Eindeutiger Key der Bestellung (intern) | [optional] 
**customer_order_id** | **string** | Individuelle Bestellnummer des Bestellers | [optional] 
**status** | **string** | Kennung des Zustandes, in dem sich die Bestellung befindet, z.B. SENT | [optional] 
**status_message** | **string** | Textuelle Zustandsbeschreibung | [optional] 
**status_date** | [**\DateTime**](\DateTime.md) | Letztes Änderungsdatum der Bestellung | [optional] 
**archived** | **bool** | Archivflag der Bestellung | [optional] 
**vendor** | [**\Boracomputer\ITScope\Model\Vendor**](Vendor.md) | Referenz auf den Verkäufer (interner Key, n:1) | 
**order** | [**\Boracomputer\ITScope\Model\Order[]**](Order.md) | Details zur Liste der &lt;a href&#x3D;\&quot;https://support.itscope.com/hc/de/articles/206814239\&quot;&gt;OpenTrans 2.1 ORDER&lt;/a&gt; Dokumente | [optional] 
**orderresponse** | [**\Boracomputer\ITScope\Model\Orderresponse[]**](Orderresponse.md) | Details zur Liste der &lt;a href&#x3D;\&quot;https://support.itscope.com/hc/de/articles/206814239\&quot;&gt;OpenTrans 2.1 ORDERRESPONSE&lt;/a&gt; Dokumente | [optional] 
**dispatchnotification** | [**\Boracomputer\ITScope\Model\Dispatchnotification[]**](Dispatchnotification.md) | Details zur Liste der &lt;a href&#x3D;\&quot;https://support.itscope.com/hc/de/articles/206814239\&quot;&gt;OpenTrans 2.1 DISPATCHNOTIFICATION&lt;/a&gt; Dokumente | [optional] 
**invoice** | [**\Boracomputer\ITScope\Model\Invoice[]**](Invoice.md) | Details zur Liste der &lt;a href&#x3D;\&quot;https://support.itscope.com/hc/de/articles/206814239\&quot;&gt;OpenTrans 2.1 INVOICE&lt;/a&gt; Dokumente | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


