https://docs.keycrm.app/ - ������������

*************** ��������� ���������� ��� keyCRM ***************

��� �������� ���������� Servio -> keyCRM   ���������� ��������� ��������� ��������:

	1. � �������� keyCRM (��������� -> �������������) ���������� �������� ������� � ���������������� ���� ��� ������� ���� string ��� 
��������� �������, ����������, ��������. ��� ���� ����� ������� �������������� ��������� � �������� �������. 
��������� ��� ���� ����� ����� ����� ������� � ����� �������� ������ �������� KeyCrmSettings � ������� IdentityCustomFields.
������:
	<IdentityCustomFields>
		<IdentityCustomFieldItem Entity="Pipeline" SystemName="OR_1003" ServioEntity="Activity" />
		<IdentityCustomFieldItem Entity="Pipeline" SystemName="OR_1002" ServioEntity="Group" />
		<IdentityCustomFieldItem Entity="Pipeline" SystemName="OR_1001" ServioEntity="Guest" />
		<IdentityCustomFieldItem Entity="Buyer" SystemName="CT_1003" />
		<IdentityCustomFieldItem Entity="Company" SystemName="CY_1002" />
	</IdentityCustomFields>
	2. � ������� ��������� -> �������� ���������� ������������ ����� ��� API. ������ ����� ����� ����� �������
� ��������� ApiKey ����� Hotel � ����� �������� ������.
	3. ����� ����������� ����� ������� �������� DefaultSourceId - ������������� ��������� �� ������� CRM.
������ �������� �������� ������������ ��� �������� ������.
	4. ������� ������������� ������������ � ������� CRM, ��� ������� ����� ����������� ������ � ��������� DefaultCrmOrderManager.
	5. ��� ����������� ���������� ������� � ����� �� ��������� ��������� �������� ������� ���������� ��������� �������
����� ����� � ��������� ������� CRM � ����� ServiceMapping. ������:
			<ServiceMapping>
				<ServiceMappingItem CrmValue="2">
					<Services>573</Services>
				</ServiceMappingItem>
			</ServiceMapping>

	�������:

	����� ����� �������� ����� �� ������������ ������� �� ��������� KeyCrmMappingApp ��� ������ � ����� � ����� KeyCrm

