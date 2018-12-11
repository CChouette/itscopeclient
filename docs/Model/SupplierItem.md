# SupplierItem

## Properties
Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **int** | Eindeutiger Key | 
**ean** | **string** | EAN-Angabe des Lieferanten | [optional] 
**manufacturer_sku** | **string** | Hersteller-Artikelnummer-Angabe des Lieferanten (muss nicht mit ITscope übereinstimmen) | [optional] 
**supplier_sku** | **string** | Produktnummer des Lieferanten | [optional] 
**supplier_id** | **int** | Verweist 1:1 auf Supplier.id | 
**supplier_name** | **string** | Name des Lieferanten | [optional] 
**manufacturer_name** | **string** | Herstellername wie beim Lieferant angegeben | [optional] 
**product_name** | **string** | Genauer Bezeichner des Artikels, wie vom Lieferanten übermittelt | [optional] 
**long_description** | **string** | Erweiterte Artikelbeschreibung des Lieferanten | [optional] 
**condition_id** | **int** | Numerischer Code des &lt;a href&#x3D;\&quot;https://support.itscope.com/hc/de/articles/207167615\&quot;&gt;Zustand des Artikels&lt;/a&gt; | 
**condition_name** | **string** | &lt;a href&#x3D;\&quot;https://support.itscope.com/hc/de/articles/207167615\&quot;&gt;Zustand des Artikels&lt;/a&gt; (neu, gebraucht, B-Ware, Refurbished, usw.) | 
**eol_product** | **bool** | Kennung: Auslaufartikel | 
**match_quality** | **int** | &lt;a href&#x3D;\&quot;https://support.itscope.com/hc/de/articles/206175301\&quot;&gt;Zuordnungsqualität&lt;/a&gt; des Artikels zum ITscope-Produktkatalog | 
**ean_valid** | **bool** | Flag, ob die EAN des Lieferanten valide nach den EAN-Kriterien ist | 
**special_offer** | **bool** | Flag, ob Artikel Sonderangebot ist | 
**promotion** | **string** | Name der Promo-Aktion des Lieferanten | [optional] 
**vat** | **int** | MwSt-Satz für den Artikel | [optional] 
**copyright_levy** | **double** | Urheberrechtsabgabe | [optional] 
**customs_tariff_number** | **string** | Zolltarifnummer | [optional] 
**country_of_origin** | **string** | Ursprungsland des Artikels | [optional] 
**gross_dim_x** | **double** | LÄnge des Produkts inklusive Maßeinheit | [optional] 
**gross_dim_y** | **double** | Höhe des Produks inklusive Maßeinheit | [optional] 
**gross_dim_z** | **double** | Breite des Produkts inklusive Maßeinheit | [optional] 
**warranty_text** | **string** | Garantieangaben des Lieferanten | [optional] 
**deeplink** | **string** | Link zum Artikel beim Lieferanten | [optional] 
**recommended_retail_price_net** | **double** | UVP-Angabe des Lieferanten | [optional] 
**price** | **double** | Preis | [optional] 
**price_calc** | **double** | Kalkulierter Preis, auf Grundlage der individuellen &lt;a href&#x3D;\&quot;https://support.itscope.com/hc/de/sections/201887801\&quot;&gt;Preiskalkulation&lt;/a&gt; | [optional] 
**currency_code** | **string** | Währungseinheit, die für diese Preisinformation gilt | [optional] 
**price_calc_vat** | **double** | Umsatzsteuersatz, der zur Berechnung des &lt;a href&#x3D;\&quot;https://support.itscope.com/hc/de/articles/206156619\&quot;&gt;kalkulierten Preises&lt;/a&gt; benutzt wurde | [optional] 
**price_last_update** | [**\DateTime**](\DateTime.md) | Zeitpunkt der letzten Aktualisierungs der Preisinformation | [optional] 
**stock_supplier_text** | **string** | Bestandsinformation zur Bezugsquelle, wie vom Lieferanten übermittelt | [optional] 
**stock_status** | **int** | Numerischer Schlüssel des &lt;a href&#x3D;\&quot;https://support.itscope.com/hc/de/articles/207168445\&quot;&gt;Lieferstatus dieser Bestandsinformation&lt;/a&gt; | [optional] 
**stock_status_text** | **string** | &lt;a href&#x3D;\&quot;https://support.itscope.com/hc/de/articles/207168445\&quot;&gt;Lieferstatus dieser Bestandsinformation&lt;/a&gt;, z.B. \&quot;auf Lager\&quot; oder \&quot;im Außenlager\&quot; | [optional] 
**stock** | **int** | Bestandsmenge | [optional] 
**external_stock** | **int** | Im Außenlager befindliche Bestandsmenge (Zusatzinformation einiger Lieferanten in Strukturen des Lieferstatus \&quot;auf Lager\&quot;) | [optional] 
**incoming_stock** | **int** | Im Zulauf befindliche Bestandsmenge  (Zusatzinformation einiger Lieferanten in Strukturen des Lieferstatus \&quot;auf Lager\&quot;) | [optional] 
**stock_availability_date** | [**\DateTime**](\DateTime.md) | Liefertermin für nicht auf Lager befindliche Ware | [optional] 
**last_stock_update** | [**\DateTime**](\DateTime.md) | Zeitpunkt der letzten Aktualisierung der Bestandsinformation | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


