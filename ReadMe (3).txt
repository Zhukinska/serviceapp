https://docs.keycrm.app/ - документация

*************** Настройка интеграции для keyCRM ***************

Для успешной интеграции Servio -> keyCRM   необходимо выполнить следующие действия:

	1. В кабинете keyCRM (Настройки -> Дополнительно) необходимо добавить воронки и пользовательские поля для каждого типа string для 
сущностей воронки, покупателя, компании. Эти поля будут хранить идентификаторы сущностей в отельной системе. 
Системное имя этих полей нужно будет указать в файле настроек модуля стыковки KeyCrmSettings в разделе IdentityCustomFields.
Пример:
	<IdentityCustomFields>
		<IdentityCustomFieldItem Entity="Pipeline" SystemName="OR_1003" ServioEntity="Activity" />
		<IdentityCustomFieldItem Entity="Pipeline" SystemName="OR_1002" ServioEntity="Group" />
		<IdentityCustomFieldItem Entity="Pipeline" SystemName="OR_1001" ServioEntity="Guest" />
		<IdentityCustomFieldItem Entity="Buyer" SystemName="CT_1003" />
		<IdentityCustomFieldItem Entity="Company" SystemName="CY_1002" />
	</IdentityCustomFields>
	2. В разделе Настройки -> Основные необходимо сгенерирвать токен для API. Данный токен нужно будет указать
в параметре ApiKey блока Hotel в файле настроек модуля.
	3. Также обязательно нужно указать параметр DefaultSourceId - идентификатор источника из системы CRM.
Данный параметр является обязательным при создании заказа.
	4. Указать идентификатор пользователя в системе CRM, под которым будут создаваться заказы в параметре DefaultCrmOrderManager.
	5. Для возможности добавления товаров в заказ на основании наислений отельной системы необходимо выполнить маппинг
услуг отеля и продуктов системы CRM в блоке ServiceMapping. Пример:
			<ServiceMapping>
				<ServiceMappingItem CrmValue="2">
					<Services>573</Services>
				</ServiceMappingItem>
			</ServiceMapping>

	Примітка:

	Також можна виконати майже всі налаштування системи за допомогою KeyCrmMappingApp яка додана в архів в папці KeyCrm

