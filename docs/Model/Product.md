# Product

## Properties
Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**puid** | **int** | Eindeutiger Key | 
**ean** | **string** | EAN | [optional] 
**manufacturer_sku** | **string** | Herstellerartikelnummer | [optional] 
**icecat_id** | **string** | IceCat ID | [optional] 
**cnet_id** | **string** | CNET ID | [optional] 
**bechlem_id** | **string** | Bechlem ID | [optional] 
**e_class** | **string** | eClass ID | [optional] 
**manufacturer_id** | **int** | Referenz auf den Hersteller dieses Produktes (n:1 auf Manufacturer.id) | 
**manufacturer_name** | **string** | Name des Herstellers | [optional] 
**product_name_with_manufacturer** | **string** | &lt;a href&#x3D;\&quot;https://support.itscope.com/hc/de/articles/206554329\&quot;&gt;Produktname&lt;/a&gt;, inklusive Herstellername | 
**short_description** | **string** | &lt;a href&#x3D;\&quot;https://support.itscope.com/hc/de/articles/206554329\&quot;&gt;Kurzbezeichner&lt;/a&gt; des Produktes | [optional] 
**long_description** | **string** | &lt;a href&#x3D;\&quot;https://support.itscope.com/hc/de/articles/206554329\&quot;&gt;Langtext&lt;/a&gt; des Produktes | [optional] 
**product_type_id** | **int** | Referenz auf den Produkttyp dieses Produktes | 
**product_type_group_id** | **string** | Referenz auf Produkttyp-Gruppe (ProductTypeGroup.id, n:1) | 
**product_type_group_name** | **string** | Name der Gruppe von Produkttypen, z.B. Netzwerktechnik. Kann als 1. &lt;a href&#x3D;\&quot;https://support.itscope.com/hc/de/articles/207249385\&quot;&gt;Kategorieebene&lt;/a&gt; verwendet werden. | 
**product_type_name** | **string** | Bezeichner des Produkttyps. Kann als 2. &lt;a href&#x3D;\&quot;https://support.itscope.com/hc/de/articles/207249385\&quot;&gt;Kategorieebene&lt;/a&gt; verwendet werden. | 
**attribute_type_id1** | **int** | Eindeutiger Attribut Key, um eine mögliche Unterkategorie aufzubauen, verweist 1:n auf AttributeCluster.attributeTypeId | [optional] 
**attribute_type_name1** | **string** | Bezeichner des Attributes, um eine mögliche Unterkategorie aufzubauen | [optional] 
**attribute_type_id2** | **int** | Eindeutiger Attribut Key, um eine mögliche Unterkategorie aufzubauen, verweist 1:n auf AttributeCluster.attributeTypeId | [optional] 
**attribute_type_name2** | **string** | Bezeichner des Attributes, um eine mögliche Unterkategorie aufzubauen | [optional] 
**attribute_type_id3** | **int** | Eindeutiger Attribut Key, um eine mögliche Unterkategorie aufzubauen, verweist 1:n auf AttributeCluster.attributeTypeId | [optional] 
**attribute_type_name3** | **string** | Bezeichner des Attributes, um eine mögliche Unterkategorie aufzubauen | [optional] 
**attribute_type_id4** | **int** | Eindeutiger Attribut Key, um eine mögliche Unterkategorie aufzubauen, verweist 1:n auf AttributeCluster.attributeTypeId | [optional] 
**attribute_type_name4** | **string** | Bezeichner des Attributes, um eine mögliche Unterkategorie aufzubauen | [optional] 
**attribute_type_id5** | **int** | Eindeutiger Attribut Key, um eine mögliche Unterkategorie aufzubauen, verweist 1:n auf AttributeCluster.attributeTypeId | [optional] 
**attribute_type_name5** | **string** | Bezeichner des Attributes, um eine mögliche Unterkategorie aufzubauen | [optional] 
**attribute_value1** | **string** | Eigenschaftswert für das Attribut aus ProductType.attributeTypeId1. Kann, falls vorhanden, als 3. &lt;a href&#x3D;\&quot;https://support.itscope.com/hc/de/articles/207249385\&quot;&gt;Kategorieebene&lt;/a&gt; verwendet werden. | [optional] 
**attribute_value2** | **string** | Eigenschaftswert für das Attribut aus ProductType.attributeTypeId2. Kann, falls vorhanden, als 4. &lt;a href&#x3D;\&quot;https://support.itscope.com/hc/de/articles/207249385\&quot;&gt;Kategorieebene&lt;/a&gt; verwendet werden. | [optional] 
**attribute_value3** | **string** | Eigenschaftswert für das Attribut aus ProductType.attributeTypeId3. Kann, falls vorhanden, als 5. &lt;a href&#x3D;\&quot;https://support.itscope.com/hc/de/articles/207249385\&quot;&gt;Kategorieebene&lt;/a&gt; verwendet werden. | [optional] 
**attribute_value4** | **string** | Eigenschaftswert für das Attribut aus ProductType.attributeTypeId4 | [optional] 
**attribute_value5** | **string** | Eigenschaftswert für das Attribut aus ProductType.attributeTypeId5 | [optional] 
**product_sub_type_id** | **string** | ID der Bauart-Eigenschaft | [optional] 
**product_sub_type** | **string** | Bauart-Eigenschaft des Produktes, z.B. Maus oder Tastatur für Eingabegeräte. Sollte &lt;b&gt;nicht&lt;/b&gt; als 3. &lt;a href&#x3D;\&quot;https://support.itscope.com/hc/de/articles/207249385\&quot;&gt;Kategorieebene&lt;/a&gt; verwendet werden. | [optional] 
**product_line_id** | **int** | ID der Produktlinie | [optional] 
**product_line** | **string** | Produktlinie | [optional] 
**product_model** | **string** | Produktmodellbezeichner | [optional] 
**estimate_gross_weight** | **double** | Gewicht in Kilogramm | [optional] 
**gross_dim_x** | **string** | Länge des Produkts inklusive Maßeinheit | [optional] 
**gross_dim_y** | **string** | Höhe des Produks inklusive Maßeinheit | [optional] 
**gross_dim_z** | **string** | Breite des Produkts inklusive Maßeinheit | [optional] 
**customs_tariff_number** | **string** | Zolltarifnummer | [optional] 
**deeplink** | **string** | Deeplink auf die ITscope.com Plattform | 
**standard_html_datasheet** | **string** | URL, Link auf HTML Standard-Datenblatt | 
**standard_pdf_datasheet** | **string** | URL, Link auf PDF Standard-Datenblatt | [optional] 
**manufacturer_site** | **string** | URL, Link auf Herstellerseite | [optional] 
**manufacturer_datasheet** | **string** | URL, Link auf Herstellerdatenblatt | [optional] 
**image_thumb** | **string** | Vorschau des besten &lt;a href&#x3D;\&quot;https://support.itscope.com/hc/de/articles/206430869\&quot;&gt;Produktbildes&lt;/a&gt; | [optional] 
**image_thumb_width** | **int** | Breite des Bild Mediums in Pixel | [optional] 
**image_thumb_height** | **int** | Höhe des Bild Mediums in Pixel | [optional] 
**image1** | **string** | Link auf bestmögliches &lt;a href&#x3D;\&quot;https://support.itscope.com/hc/de/articles/206430869\&quot;&gt;Bild&lt;/a&gt;, in der größten Ausführung | [optional] 
**image_width1** | **int** | Breite des Bild Mediums in Pixel | [optional] 
**image_height1** | **int** | Höhe des Bild Mediums in Pixel | [optional] 
**image2** | **string** | Link auf ein weiteres gutes &lt;a href&#x3D;\&quot;https://support.itscope.com/hc/de/articles/206430869\&quot;&gt;Produktbild&lt;/a&gt;, bevorzugt das einer Produktverpackung (nie das gleiche wie das erste Bild) | [optional] 
**image_width2** | **int** | Breite des Bild Mediums in Pixel | [optional] 
**image_height2** | **int** | Höhe des Bild Mediums in Pixel | [optional] 
**image3** | **string** | Link auf erstes &lt;a href&#x3D;\&quot;https://support.itscope.com/hc/de/articles/206430869\&quot;&gt;Bild&lt;/a&gt; in der Galerie (niemals eines der bereits aufgeführten) | [optional] 
**image_width3** | **int** | Breite des Bild Mediums in Pixel | [optional] 
**image_height3** | **int** | Höhe des Bild Mediums in Pixel | [optional] 
**image4** | **string** | Link auf zweites &lt;a href&#x3D;\&quot;https://support.itscope.com/hc/de/articles/206430869\&quot;&gt;Bild&lt;/a&gt; in der Galerie (niemals eines der bereits aufgeführten) | [optional] 
**image_width4** | **int** | Breite des Bild Mediums in Pixel | [optional] 
**image_height4** | **int** | Höhe des Bild Mediums in Pixel | [optional] 
**image5** | **string** | Link auf drittes &lt;a href&#x3D;\&quot;https://support.itscope.com/hc/de/articles/206430869\&quot;&gt;Bild&lt;/a&gt; in der Galerie (niemals eines der bereits aufgeführten) | [optional] 
**image_width5** | **int** | Breite des Bild Mediums in Pixel | [optional] 
**image_height5** | **int** | Höhe des Bild Mediums in Pixel | [optional] 
**energy_label** | **string** | Link auf das Energielabel &lt;a href&#x3D;\&quot;https://support.itscope.com/hc/de/articles/206430869\&quot;&gt;Bild&lt;/a&gt; | [optional] 
**entry_date** | [**\DateTime**](\DateTime.md) | Ab wann ist das Produkt auf der Plattform | 
**rank** | **int** | Allgemeiner Beliebtheitsrang (Rang 1 bis n, eine hohe Zahl entspricht einem schlechten Ranking) | [optional] 
**qualification** | **int** | &lt;a href&#x3D;\&quot;https://support.itscope.com/hc/de/articles/206032562\&quot;&gt;Qualifizierung des Produkts&lt;/a&gt; | [optional] 
**warranty_text** | **string** | &lt;a href&#x3D;\&quot;https://support.itscope.com/hc/de/articles/206554329\&quot;&gt;Garantietext&lt;/a&gt; des Produktes | [optional] 
**marketing_text** | **string** | &lt;a href&#x3D;\&quot;https://support.itscope.com/hc/de/articles/206554329\&quot;&gt;Marketingtext&lt;/a&gt; für das Produkt | [optional] 
**html_specs** | **string** | &lt;a href&#x3D;\&quot;https://support.itscope.com/hc/de/articles/206525469\&quot;&gt;Technische Eigenschaften&lt;/a&gt; des Produktes, im HTML Format | [optional] 
**recommended_retail_price_net** | **double** | UVP des Herstellers | [optional] 
**price** | **double** | Preisbasis für den &lt;a href&#x3D;\&quot;https://support.itscope.com/hc/de/articles/206156619\&quot;&gt;kalkulierten Preis&lt;/a&gt; | [optional] 
**price_calc** | **double** | Kalkulierter Preis, auf Grundlage der individuellen &lt;a href&#x3D;\&quot;https://support.itscope.com/hc/de/sections/201887801\&quot;&gt;Preiskalkulation&lt;/a&gt; | [optional] 
**currency_code** | **string** | Währungseinheit, die für diese Preisinformation gilt | [optional] 
**price_calc_vat** | **double** | Umsatzsteuersatz, der zur Berechnung des &lt;a href&#x3D;\&quot;https://support.itscope.com/hc/de/articles/206156619\&quot;&gt;kalkulierten Preises&lt;/a&gt; benutzt wurde | [optional] 
**price_last_update** | [**\DateTime**](\DateTime.md) | Zeitpunkt der letzten Aktualisierungs der Preisinformation | [optional] 
**price_supplier_id** | **int** | Referenz auf einen Lieferanten (1:1), der die Bezugsquelle mit dieser Preisinformation bereitgestellt hat | [optional] 
**price_supplier_name** | **string** | Name des Lieferanten, der diese Bezugsquelle bereitgestellt hat | [optional] 
**price_supplier_item_id** | **int** | Referenz auf eine Bezugsquelle (n:1); wenn dieses Feld null ist, dann bezieht sich die Preisinformation auf ein Produkt (Bezugsquellenrefernz und Produktrefernz schließen sich gegenseitig aus) | [optional] 
**price_supplier_sku** | **string** | Produktbezeichner des Lieferanten, der diese Bezugsquelle bereitgestellt hat | [optional] 
**stock_supplier_text** | **string** | Textuelle Bestandsinformation des Lieferanten, direkt übernommen, ohne Interpretation | [optional] 
**stock_status** | **int** | Numerischer Schlüssel des &lt;a href&#x3D;\&quot;https://support.itscope.com/hc/de/articles/207168445\&quot;&gt;Lieferstatus dieser Bestandsinformation&lt;/a&gt; | [optional] 
**stock_status_text** | **string** | &lt;a href&#x3D;\&quot;https://support.itscope.com/hc/de/articles/207168445\&quot;&gt;Lieferstatus dieser Bestandsinformation&lt;/a&gt;, z.B. \&quot;auf Lager\&quot; oder \&quot;im Außenlager\&quot; | [optional] 
**stock** | **int** | Bestandsmenge des in dieser Struktur angegebenen Lieferstatus | [optional] 
**external_stock** | **int** | Im Außenlager befindliche Bestandsmenge (Zusatzinformation einiger Lieferanten in Strukturen des Lieferstatus \&quot;auf Lager\&quot;) | [optional] 
**incoming_stock** | **int** | Im Zulauf befindliche Bestandsmenge  (Zusatzinformation einiger Lieferanten in Strukturen des Lieferstatus \&quot;auf Lager\&quot;) | [optional] 
**stock_availability_date** | [**\DateTime**](\DateTime.md) | Liefertermin für nicht auf Lager befindliche Ware | [optional] 
**stock_last_update** | [**\DateTime**](\DateTime.md) | Zeitpunkt der letzten Aktualisierung der Bestandsinformation | [optional] 
**aggregated_status** | **int** | Bester Verfügbarkeitsstatus | 
**aggregated_status_text** | **string** | Bester Verfügbarkeitsstatus | 
**aggregated_stock** | **int** | Summe aller Lagerbestände | 
**aggregated_supplier_items** | **int** | Summe aller Distributoren zu diesem Produkt | 
**supplier_item** | [**\Swagger\Client\Model\SupplierItem[]**](SupplierItem.md) | Bezugsquelle eines ITscope-Produkts. Ein konkretes Angebot eines auf ITscope gelisteten Distributors. | 
**attribute** | [**\Swagger\Client\Model\Attribute[]**](Attribute.md) | Eigenschaften zu einem Produkt. | [optional] 
**attribute_cluster** | [**\Swagger\Client\Model\AttributeCluster[]**](AttributeCluster.md) | Eigenschaftscluster, in denen das Produkt für Merkmalssuchen gefunden werden kann. Kann je nach Menge mehrere Eigenschaftsausprägungen in Intervallen zusammenfassen, z.B. 64-128MB RAM | [optional] 
**accessory** | [**\Swagger\Client\Model\Accessory[]**](Accessory.md) | &lt;a href&#x3D;\&quot;https://support.itscope.com/hc/de/articles/206032592\&quot;&gt;Originalzubehör und kompatibles Zubehör&lt;/a&gt; zu einem Produkt | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


