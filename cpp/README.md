TlvObject
----------

An easy-to-use TLV API in C plus plus

Building
----------

    g++ -o Test.cpp TlvObject.cpp 
    ./test

Usage
----------

 **1. Public functions for encode**

    //Put one TLV box
    bool PutCharValue(int type,const char &value);
    bool PutShortValue(int type,const short &value);
    bool PutIntValue(int type,const int &value);
    bool PutLongValue(int type,const long &value);
    bool PutLongLongValue(int type,const long long &value);
    bool PutFloatValue(int type,const float &value);
    bool PutDoubleValue(int type,const double &value);
    bool PutStringValue(int type,const char *value);
    bool PutBytesValue(int type,const unsigned char *value,int length);
    bool PutObjectValue(int type,const TlvObject& value);
    bool PutValue(int type,const void *value,int length);     
    
    //do encode
    bool Serialize(); 
    
    //access encoded buffer and length
    unsigned char * GetSerializedBuffer() const;
    int GetSerializedBytes() const;

 **2. Public functions for decode**
 
    //do decode
    bool Parse(const unsigned char *buffer,int buffersize); 
    
    //Get one TLV box
    bool GetCharValue(int type,char &value) const;
    bool GetShortValue(int type,short &value) const;
    bool GetIntValue(int type,int &value) const;
    bool GetLongValue(int type,long &value) const;
    bool GetLongLongValue(int type,long long &value) const;
    bool GetFloatValue(int type,float &value) const;
    bool GetDoubleValue(int type,double &value) const;
    bool GetStringValue(int type,char *value,int &length) const;
    bool GetBytesValue(int type,unsigned char *value,int &length) const;
    bool GetBytesValuePtr(int type,unsigned char **value,int &length) const;
    bool GetObjectValue(int type,TlvObject& value) const;
    bool GetValue(int type,const void **value,int& length) const;

 **3. Sample code**
 
     Please refer to Test.cpp.

Contact
----------
Email：lujun.hust@gmail.com