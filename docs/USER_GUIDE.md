# Operator Guide — Current Release

## Scope

This guide covers the current El Marakby Import Operations Control Tower release published at:

https://aagelghobashy-byte.github.io/elmarakby-import-control-tower/

It is a browser-local control tool. It does not replace SAP/ERP, NAFEZA, CargoX, customs broker records, accounting, warehouse or inventory systems.

## Start of day

1. Open the approved HTTPS URL.
2. Confirm the release title and current date/time in the header.
3. Review Dashboard alerts for ACID missing/pending, overdue ETA and critical shipments.
4. Export a full backup before making material edits.
5. Confirm that you are using the intended browser profile/device.

## Shipment workflow

1. Open **New Shipment**.
2. Select the legal entity.
3. Complete supplier, PI, value, currency, incoterms, payment, logistics, ETD/ETA, package and weight information.
4. Add commodity line items and verify HS information against the approved customs source. The tool does not make a legally final classification.
5. Use **Save Draft** while collecting information.
6. Use **Register Shipment → Add to Dashboard** only after the business owner accepts the record.
7. Open **Shipment Tracker** and record stage dates and notes.
8. Run **Gate Check** before relying on the ACID workflow.

## ACID / NAFEZA

1. Select the shipment in the ACID tab.
2. Complete exporter, country, ETD, issuance and ACID fields.
3. Verify the number in the official NAFEZA channel outside this tool.
4. Record document confirmations and send the ACID reference through the approved business channel.
5. Save the ACID record and confirm the dashboard reflects the status.

The current release performs client-side checks and manual recordkeeping. It does not submit to NAFEZA or CargoX automatically.

## Documents

1. Select a shipment in **Documents**.
2. Record version, status, receipt date, reviewer, approval date, originals and bank details.
3. Keep the actual source documents in the approved document repository.
4. Save the checklist only after the source documents have been reviewed.

## Customs and delivery

1. Select a shipment in **Customs**.
2. Record declaration, assessment, duty/tax, release and broker information from the authoritative customs record.
3. Record delivery and GRN information only after physical receipt and approved confirmation.
4. Save the record and export a backup when closing a shipment.

## Costs

1. Select a shipment in **Costs**.
2. Enter source costs: FOB, freight, exchange rate, duty, VAT, CargoX, broker, THC, inland and other approved costs.
3. Review the calculated CIF, taxes, miscellaneous cost, total and cost-per-ton.
4. Reconcile the result to Finance/ERP before using it for a financial decision.

## Backup and recovery

- Use the header download control for a full JSON backup.
- Use the restore/import control only after exporting the current data first.
- Keep backup files dated and access-controlled.
- Browser storage is device/profile-specific; it is not a shared backup service.

## What the operator must not do

- Do not enter credentials, API keys or payment data.
- Do not treat a green client-side gate as server authorization.
- Do not rely on a dashboard number without checking the underlying evidence.
- Do not delete all shipments or factory-reset without a verified backup.
- Do not claim an external integration is live unless the integration has been separately tested and approved.
