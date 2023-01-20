# dab

## Spec. study
[ETSI DAB specificaitons](http://portal.etsi.org/broadcast/dab.asp)

![](./img/dab_protocol_stack.jpg)

### DAB system standards and guidelines

  * EN 300 401 v1.4.1 : "main DAB" standard
  * TR 101 496 : main guideline document. 3���� ������ ��������(TR 101 496-1,2,3).
  * TS 100 756 : register table, signaling value�� ����
  * TS 102 367 : CAS(conditional access system) ����
  * TS 101 757 : �׽�Ʈ ������ �׽�Ʈ ��Ʈ��Ʈ���� ���� ����
  * EN 301 700 : FM-RDS service�� tuning �� �� �ִ� ���� ������ DAB receiver�� �˷��ִ� ��� ����

### DAB receiver standards and documents

  * EN 50248: characteristics of DAB receivers
  * EACEM TR-004 : EMC directive; DAB receiver�� ���� EMC test�� specific reference, requirement, method �׸��� test condition�� �����Ѵ�.
  * EN 50255 : DAB receiver�� data decoder�鰣�� �������̽��� ����.
  * EN 50320 : DAB receiver�� �����ϱ� ���� command set�� ����. �� command set�� ���� �ٸ� ������ ���� �ý��� �󿡼� �̿�Ǵ� ���� ������.
  * TR 101 758 : ���������� DAB system ����� ���� ȣȯ receiver ������ �ʼ� �ʵ带 �����ϴ� ������ ���� �Ϲ����� ��Ģ�� ���� ����.

### DAB transmission and network standards and documents
![](./img/800px-conceptualdabnetworkandstandards.jpg)

  * EN 300 797 : STI(service transport interface)�� ���� DAB service component, service information, control information�� ������ ���� ǥ��ȭ�� ����� �����Ѵ�.
  * TS 101 860 : EN 300 797���� ���ǵ� ����� ������ �̿뿡 ���� ���̵�
  * EN 300 798 : DAB SFN���� �� �۽� ����Ʈ�� ��ġ�� �������� DAB ä�� �ڵ����� �̿�ȴ�. �� ǥ���� DAB OFDM generator�� �� ��(baseband processing equipment, RF modulator) �ֿ� ��ҿ� �˸´� �������̽� Ư���� �����Ѵ�.
  * ETS 300 799 : �ӻ�� ��Ƽ�÷����� SFN ���� ����Ʈ�� ��ġ�� DAB ���� ��ġ ���̿� DAB ��ȣ ��ġ ����� �����Ѵ�.
  * "MINIMUM requirements for Terrestrial DAB Transmitters" : EN 300 401�� ������ ������ DAB ���۱��� �ּ� �䱸���� ����
  * EBU BPN 003 : ��Ʈ��ũ ����� ������ DAB �� ��ȹ�� ���� ������ ���� �� �Ķ���͵��� ����Ѵ�.

### Additional DAB standards and documents for data transmission

  * EN 301 234 : DAB �ý��ۿ��� �̿��ϴ� �پ��� ������ �����͸� ��ε�ĳ���� �� �� �ְ� �ϴ� MOT protocol�� ����
  * TR 101 497 : MOT version 1.xx�� ���̵带 ����. version 2.11�� ���� ������ MOT specification���� �������.
  * TS 101 498 : ���񽺵鿡 ���� ������ �����ϱ� ���� ����Ʈ �������� HTML�� �̿��� �� �ֵ��� DAB broadcast Web Site application�� ���� �����Ѵ�.
  * TS 101 499 : �̹����� ���� ������ �Բ� �����̵� �̹����� �����ϱ� ���� �䱸�Ǵ� ������� ����; MOT SlideShow; User Application Specification;
  * TS 101 759 : Eureka Project 147�� ���� ������� �� ������ DAB ���� ���� ������ �����ϰ� �����͸� �����ϱ� ���� �䱸�� ������� �����Ѵ�. �� �����ʹ� Ư���� DAB ���� bearer�� � �ٸ� �Ķ���͵鿡 ���õ� �ʿ䰡 ����.
  * ES 201 735 : DAB packet mode ���� ������Ʈ���� IP diagram�� �����ϴ� ��� ���
  * ES 201 736 : local interactive service, one-way interactive service, two-way interactive service�� ���ǵ� ���񽺵鿡�� �̿�Ǵ� �������� ������ �����Ѵ�. �׸��� DAB cell�� ���̿� �ڵ������ ����� ��ɰ� ���ǵ��� ������ ���� PSSC(Personal DAB Service Session Control) ���������� �����Ѵ�.
  * ES 201 737 : Global System for Mobile communication(GSM), Public Switched Telecommunications System(PSTN), Integrated Services Digital Network(ISDN) �׸��� Digital Enhanced Cordless Telecommunications(DECT)�� ���� Interaction Channel ������ ����
  * TS 101 993 : java�� ���� APIs
  * TS 102 818 : EPG(Electronic Programme Guide)�� ���� XML scheme data model
  * TS 102 371 : ���ű��� ������ ���� �뷮 ������ ������ ��� ���� ��Ʈ����Ʈ�� ���ҽ�Ű�� ���� DAB ���� ä�� ���� ����� EPG(Electronic Programme Guide) �����͸� ��
  * TS 102 368 : DAB ���� ä���� ���� TMC data�� ���۰� signaling ��
  * TS 102 427 : RS FEC�� �����Ͽ�, DAB MSC stream data sub-channel ���� MPEG 2 TS�� encapsulate �ϴ� ��� ��
  * TS 102 428 : DAB�� ���� video ���񽺸� �����ϴ� ����� ���뿡 ���� ��
  * TS 102 980 : DL plus ��
  * TS 103 736 : Rules of implementation; Service Information Features;